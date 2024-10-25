# Lab 03: LLM Security, Writing Defense Prompts
## Why Does LLM Security Matter?
Many security risks in LLMs arise due to their training procedure. The training procedure is roughly split into two phases: pretraining and fine tuning. During pretraining, LLMs use next-word prediction, often on large amounts of text data from the internet. Since this dataset is so large, it's difficult to ensure all of the data is high quality, and as such, the pretraining dataset may contain harmful content, which propagates into model inference. For this reason, it's crucial to manage potential stereotypes and biases during the pretraining phase. Although LLMs have varying use cases and come in various forms (e.g., public models like ChatGPT, corporate models, domain-specific models), they all share a common requirement: they must be accurate, unbiased, and robust. Therefore, ongoing research on defense, alignment, and safety is vital.

## Lab Context 
This lab is similar to Lab 02, but instead of writing attack prompts, you will be creating a single defense prompt. The only restriction is that it must fit within the system message of the LLM.

Make this defense prompt as secure as possible. We will run two attacks created by the course staff on your defense. You will receive full credit if your defense successfully blocks both attacks.

## Common Defense Tactics
Here are some common techniques used to enhance the robustness of LLMs, improving their defensive capabilities: 
1. **Safety Instructions/Constitutions:** Chat-based LLMs are trained and effective at following instructions. Simply providing safety instructions alongside user input is a valid defense strategy. 
2. **Adversarial Prompting:** Within the instructions, include adversarial concepts. Instruct the model to identify and properly respond to these. 
3. **Post Prompting:** The order of instructions can significantly impact the outcome. Placing task instructions at the end may increase the model's likelihood of following them.
4. **Output Sanitization:** Monitor the output to detect and remove any harmful or unwanted information. 	
