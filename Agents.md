# What are Agents 
Agents are AI models capable of reasoning, planning, and interacting with the env. </br>

Agents are called so because they have **"agency"**, aka it is able to interact with the env. </br>

**So the formal definition is:** An Agent is a system that leverages an AI model to interact with its environment in order to achieve a user-defined objective. It combines reasoning, planning, and the execution of actions (often via external tools) to fulfill tasks.

Think of agents as having two part: </br>
1. The brain (AI model) which is capable of thinking, reasoning and planning.
2. The body (capabilities and tools) the agent is equipped with. </br>

>[!Note]
>The scope of what the agent can do depends on what the agent has been equipped with. </br>

# Agents Workflow

The model starts by reading files, directories, code, etc. and then: </br>
Think (reasoning & planning)  -> act (execute) -> observe.

# Spectrum of Agency 
*Agency* is how much freedom the agent has to do actions without human telling it what to do. </br>

**Level of Agency** </br>

<img width="958" height="295" alt="image" src="https://github.com/user-attachments/assets/7ac76ff7-e422-4c76-859e-7d935f2307fc" /> </br>
1. Simple processor -> gives information but does not define what happen next (e.g., AI analyses and HTTP response and summarizes it)
2. Router -> AI chooses between pre-defined paths (e.g., AI decides whether an endpoint needs authentication or input validation)
3. Tool caller -> chooses which tool to execute with which parameters (e.g., AI decides to run ffuf against an authorized test)
4. Multi-step agent -> AI decides what to do next, repeats actions, and when to stop (e.g., AI discovers endpoints, selects tests, runs tools, analyzes results, and continues testing)
5. Multi-agent -> One AI agent can start another AI agent to perform a task (e.g., A reconnaissance agent delegates vulnerability testing to another specialized agent)

# Execution System

There are two main approaches to building AI agents: </br>
- Code-based frameworks (e.g., CrewAI): You write code to define the agent's behavior, workflow, tools, and execution logic. The framework provides the underlying infrastructure.
- Agentic CLIs (e.g., Claude Code, Codex, Pi): The execution system is already built. You customize the agent's behavior through natural-language instructions, skills, rules, and configuration files.

Key difference: With frameworks, you program how the agent operates. With agentic CLIs, you configure an existing agent to perform your tasks.

# AI Models 
AI models come in different types depending on what they are designed to do, what data they process, and what they proceed. </br>

| AI Model Type | What it does | Examples | Where it's used |
|---|---|---|---|
| **Large Language Models (LLMs)** | Understand and generate language, reason, and write code | GPT, Claude, Llama | Chatbots, coding assistants, AI agents |
| **Image Generation Models** | Generate or edit images from instructions | GPT Image, Stable Diffusion, FLUX | Graphic design, marketing, image editing |
| **Computer Vision Models** | Analyze and understand images or videos | YOLO, ResNet, SAM | Facial recognition, object detection, medical imaging |

The most common AI model used in Agents is **LLMs (Large Language Models)**. </br>
LLMs takes **text** as input and produces **text** as output. </br>

>[!Note]
>Vision Language Model (VLM) is like LLM but understands images as input. </br>
>It's possible to use models that accept other inputs as the agent's core model. </br>

# How Do Agents Act?
Despite agents are using LLMs which take input as text and produce output as text, they are still able to take actions. The reason is that agents leverages **tools** that help them take actions on their env. </br>
Similar to chat applications such as ChatGPT that use LLMs but still can generate images, the reason is that developers of the apps implemented additional functionality (called **tools**) that LLM can use to create images. </br>

Agents can perform any task we implement via **tools** to accomplish an action. </br>

>[!Note]
>The design of the Tools is very important and has a great impact on the quality of your Agent. </br>
>Tools are not actions. Tools are the method that help accomplishing the action. Actions are the desired objective. </br>
>Examples of agents are virtual personal assistance like Siri & Google Assistant. </br>

# What are LLMs 
