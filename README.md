# GPT Request Clarification

## Project Overview
The goal of this project is to enhance GPT models with the ability to ask clarification questions when faced with ambiguous or unclear user prompts. Instead of generating incorrect or nonsensical responses, the model will identify when it doesn't fully understand the query and ask the user for clarification. This improves the reliability and quality of responses, especially for complex or unclear inputs.

## Key Objectives
1. **Clarification Ability**: Fine-tune a GPT model to ask clarification questions when the prompt is ambiguous or unclear.
2. **Training GPT-1 and GPT-2**: Initially trained GPT-1 on a Wikipedia dataset, then fine-tuned GPT-2 using a dataset of user prompts paired with appropriate clarification responses.
3. **Evaluation**: Develop methods to assess the clarity of user prompts and evaluate how well the model responds with clarification questions.

## Dataset
1. **Wikipedia Dataset**: A large set of text data from Wikipedia articles was used for initial training of the GPT-1 model.
2. **User Prompt and Clarification Dataset**: For fine-tuning GPT-2, a dataset containing examples of user prompts that are unclear or ambiguous, along with appropriate clarification questions, was used.

## Training Details
- **GPT-1**: Initially trained on a large Wikipedia dataset to learn general language understanding.
- **GPT-2**: Fine-tuned using the following methods:
  - A dataset of unclear prompts paired with clarification questions (method a).
  - Embedding-based validation methods (method b and c) to detect ambiguous prompts.
