# How to Choose an Open-Source AI Framework for User-Facing Applications
A continually maintained framework selection guide for building customer-facing AI agents based on use case type.

This guide follows four quadrants of customer-facing use cases for AI agents.
1. ✨ Creative Agency
2. 🛠️ Task-Specific Agency
3. 🤝 Facilitative Agency
4. ✅ Aligned Agency

# Creative Agency
The bottom-left quadrant represents AI applications designed for open-ended exploration and collaborative thinking with humans. Examples are general-purpose AI assistants like ChatGPT and Claude, though more domain-specific applications will also be included here.

These systems excel at helping users explore topics, generate creative ideas—as well as engage in recreational activities—while maintaining enough structure to keep interactions meaningful and productive. A student might use these systems to understand complex topics through adaptive explanations and analogies, while professionals might employ them for brainstorming sessions that benefit from unexpected perspectives.

The recreational applications are equally valuable. Users can engage in creative writing, explore hypothetical scenarios, or seek advice on hobbies like photography or cooking.

### Frameworks
1. [LangChain](https://github.com/langchain-ai/langchain): Low-fidelity use cases with an extremely wide range of quick and easy practical integrations (PDFs, Google Docs, Office, YouTube transcriptions, and many more).
1. **Multi-agent frameworks**: Frameworks like [CrewAI](https://github.com/crewAIInc/crewAI) and [AutoGen](https://github.com/microsoft/autogen) allow you to spread a task across multiple AI personas interacting with each other. This often leads to multiple perspectives being represented in the final output, which is particularly valuable for research-oriented use cases.

# Task-Specific Agency
The top-left quadrant represents systems that adhere closely to task-specific instructions while working with a relatively broad or low number of directives. Consider how Bloomberg's financial data extraction agents reliably process vast amounts of unstructured financial information.

Organizations should consider this quadrant for tasks requiring reliable, consistent performance across varying inputs but not requiring many instructions. This is particularly valuable for data processing, automation, and extraction and analysis (ETL workflows), where accuracy is crucial while the scope of the task is narrow and well-defined.

### Frameworks
1. [Unsloth](https://github.com/unslothai/unsloth): Simplifies the process if fine-tuning Small Language Models (SLMs) and makes it more efficient. With fine-tuned SLMs, it’s demonstrably possible to reach low-cost yet high-quality, consistent results on repetitive tasks.
1. [DSPy](https://github.com/stanfordnlp/dspy) and [AdalFlow](https://github.com/SylphAI-Inc/AdalFlow): These frameworks focus on prompt optimization for specific tasks. Given a set of labeled cases with expected outputs, similarly to traditional machine-learning practices like backpropagation, they optimize prompts to achieve higher accuracy. The more well-defined your task is, the better results you’ll get from these frameworks.

# Facilitative Agency
In the bottom-right quadrant, we find AI assistants that are designed to work alongside humans in common business applications to increase efficiency and usability. These systems follow specific guidelines while maintaining enough openness and flexibility to support various user needs. At the same time, to facilitate this higher level of “give,” these systems naturally sacrifice consistent adherence to a provided set of protocols.

For example, Microsoft's Excel Copilot understands spreadsheet operations precisely but adapts to open-ended user inquiries, whether building a financial model or creating a project timeline. Salesforce's Einstein similarly enhances CRM workflows by offering specific suggestions for customer engagement. In collaborative tools like Miro, AI assistants help structure brainstorming sessions and organize information while preserving the team's creative freedom.

### Frameworks
1. [LangGraph](https://github.com/langchain-ai/langgraph) and [LlamaIndex](https://github.com/run-llama/llama_index): These frameworks allow you to separate and focus LLM’s processing into different states in your workflow. They also come with a large number of integrations, making it easier to implement impressive functionality.
1. [PydanticAI](https://github.com/pydantic/pydantic-ai): Based on the popular Pydantic library, PydanticAI is built around structured schemas. Working with schematic responses and tool calls avoids many heuristical parsing mechanisms and increases execution robustness. PydanticAI’s downside is that there are (currently) fewer integrations.

# Aligned Agency
Under this quadrant, we see customer service systems in healthcare, financial, and legal contexts, that must maintain strict compliance while handling sensitive actions and information, as well as valuable client relationships.

The Aligned Agency quadrant deserves special attention in this selection framework because it represents the highest-stakes use case. When organizations handle sensitive data, operate in regulated environments, or manage client relationships, the consequences of choosing an unsuitable framework can be paralyzing. We’ve seen cases where the wrong choice has led to teams spending several months without converging into a deployable outcome, as well as complete shutdowns of projects months into their development.

### Frameworks

1. [Rasa](https://github.com/RasaHQ/rasa): A traditional, flow-based NLU (Natural Language Understanding), Rasa is a highly deterministic framework, making it a safe choice for aligned agency use cases that do not require extensive conversational adaptability.
1. [Parlant](https://github.com/emcie-co/parlant): An LLM-native conversation design framework, Parlant focuses on enabling fine-grained control over the behavior of LLM-based agents. It achieves this using structured support for numerous behavior guidelines that are written in natural language, coupled with a runtime supervision engine that enforces behavioral configurations and optimizes for consistent conversational performance.


# Discussion
To suggest additional frameworks for consideration, please feel free to open up a PR.
