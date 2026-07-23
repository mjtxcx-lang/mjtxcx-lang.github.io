# AI实验室在"鹈鹕骑车"基准测试上作弊了吗？大规模实验给出答案

> 原文：[Are AI Labs Pelicanmaxxing?](https://dylancastillo.co/posts/pelicanmaxxing.html) | 日期：2026-07-24

Simon Willison的"鹈鹕骑自行车"SVG生成测试已成为AI圈最著名的非正式基准测试之一。研究者Dylan Castillo设计了一个系统性实验来验证各大AI实验室是否针对该测试进行了针对性训练（"Pelicanmaxxing"）。他构建了8种动物×6种交通工具的48个提示词网格，通过OpenRouter测试了GPT-5.6 Terra、Claude Sonnet 5、Gemini 3.5 Flash、Grok 4.5、Qwen3.7-Max、GLM-5.2和DeepSeek V4 Pro共7个前沿模型，生成了1008张SVG图像，并使用LLM评委进行三阶段评分。结果令人安心：鹈鹕在8种动物中排名第6，自行车在6种交通工具中排名倒数第二，均无异常高分表现。作者进行了视觉检查、动物排名、车辆排名和难度校正四项分析，均未发现任何实验室存在针对该基准测试的过拟合迹象。结论是：目前没有证据表明AI实验室在"鹈鹕骑车"上进行了benchmaxxing。
