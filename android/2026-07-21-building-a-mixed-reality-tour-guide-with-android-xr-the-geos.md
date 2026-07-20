# Building a Mixed-Reality Tour Guide with Android XR, the Geospatial API, and Gemini

**来源:** [http://android-developers.googleblog.com/2026/06/android-xr-geospatial-api-gemini.html](http://android-developers.googleblog.com/2026/06/android-xr-geospatial-api-gemini.html)

**日期:** 2026-07-21

## 中文概述

用Android XR+Geospatial API+Gemini构建混合现实导游应用

---

## 原文摘录

Android Developers Blog
The latest Android and Google Play news for app and game
Building a Mixed-Reality Tour Guide with Android XR, the Geospatial API, and Gemini
Link copied to clipboard
Posted by Coco Fatus, UX Designer, Alon Hetzroni, UX Engineer, Azin Mehrnoosh, Product Manager Android XR
At this year's Google I/O
, we announced an update for spatial experiences: the
is now available as a preview in
ARCore for Jetpack XR
. By bringing Google's Visual Positioning System (VPS) to Android XR, Android XR enables anchoring digital content to the physical world with sub-meter accuracy and precise orientation in supported areas.* To explore what the Geospatial API could unlock, our team built a demo: the XR Geospatial Tour.
Imagine walking into a new city, putting on a pair of wired XR glasses (like the upcoming XREAL Project Aura), and instantly having a knowledgeable, local guide showing you around. You don't need to stare down at a 2D map—instead, 3D models gently guide your path, and an intelligent voice tells you about the historical landmarks right in front of you. We combined the
Gemini API using Firebase AI Logic
Google Maps Grounding
to create a hands-free, immersive walking tour experience.
*Disclaimer: Video and Tour Guide application are for demonstration purposes only. Some sequences have been shortened. Any hardware depicted may be under development; final product details may differ.
Let’s walk through the implementation details and show how we tied these APIs together to build a world-scale spatial experience.
1. Pinpointing the User with ARCore Geospatial API (VPS)
Enhance your navigation experience on XR by combining the power of GPS with the precision of VPS. The accuracy and precise orientation that comes with VPS allows 3D waypoints to align with the physical world.
This is why the Geospatial API on Android XR can help you build custom experiences. By using advanced computer vision, VPS tries to provide a
(including latitude, longitude, and heading) that is more accurate than GPS.
Here's how we retrieve the user's Geospatial pose by mapping the device's orientation to a Geospatial coordinate:
// Retrieve the current geospatial pose from the ARCore session
val result = geospatial.createGeospatialPoseFromPose(arDevice.state.value.devicePose)
if (result is CreateGeospatialPoseFromPoseSuccess) {
val pose = result.pose
Log.d("VPS", "Accurate Location: ${pose.latitude}, ${pose.longitude}")
Because the entire experience relies on this accuracy, we monitor the horizontalAccuracy and orientationYawAccuracy until they meet our thresholds. If the user is indoors or in an unrecognized area, we prompt them to "walk to an outdoor public space and look around".
2. Crafting the Itinerary with Gemini API & Google Maps Grounding
Once we have a location, we use the
Gemini API using Firebase AI Logic
to prompt the Gemini model to act as a local tour guide. We pass the user's coordinates to the model and ask it to output a structured JSON response containing nearby walking tours:
val configForTools = ToolConfig(
functionCallingConfig = null,
retrievalConfig = retrievalConfig {
latLng = FirebaseLatLng(pose.latitude, pose.longitude)
val responseJsonSchema = Schema.obj(
"locationIntro" to Schema.string(),
"tours" to Schema.array(
"title" to Schema.string(),
"description" to Schema.string(),
"stops" to Schema.array(
"name" to Schema.string(),
"detailedName" to Schema.string(),
"description" to Schema.string()
val model = Firebase.ai(backend = GenerativeBackend.googleAI()).generativeModel(
modelName = "gemini-3.5-flash",
tools = listOf(Tool.googleMaps()),
generationConfig = generationConfig {
responseMimeType = "application/json"
responseSchema = responseJsonSchema
val result = model.generateContent("The user is at latitude ${pose.latitude} and longitude ${pose.longitude}. Generate exactly 3 diverse tours near this location (e.g., historical, food, nature). All tour ideas should be walking distance only.")
Large Language Models are great at generating rich descriptions, but they can sometimes hallucinate exact latitude/longitude coordinates. To solve this, we used
Google Maps Grounding
3. A Voice to Guide You: Gemini 2.5 TTS
To make the tour guide feel truly present, we implemented dynamic voiceovers.
Using the gemini-2.5-flash-tts model, we can configure our model generation config to natively return audio data instead of just text! Here’s how you can request the ResponseModality.AUDIO:
val ttsModel = Firebase.ai(backend = GenerativeBackend.googleAI())
modelName = "gemini-2.5-flash-tts",
generationConfig = generationConfig {
// Instruct the model to return Audio
responseModalities = listOf(ResponseModality.AUDIO)
val response = ttsModel.generateContent("Say in a neutral but positive voice:\n$prompt")
// Extract the raw audio bytes from the response
val audioBytes = response.candidates.firstOrNull()?.content?.parts
?.filterIsInstance<InlineDataPart>()
?.firstOrNull { it.mimeType.contains("audio") }?.inlineData
4. 
