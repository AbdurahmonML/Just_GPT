# GPT Request Clarification

## Project Overview
The goal of this project is to enhance GPT models with the ability to ask clarification questions when faced with ambiguous or unclear user prompts. Instead of generating incorrect or nonsensical responses, the model will identify when it doesn't fully understand the query and ask the user for clarification. This improves the reliability and quality of responses, especially for complex or unclear inputs.

## What I have done:
1. **Training GPT-1 from scratch**: Initially trained GPT-1 on a Wikipedia dataset with num_layers = 6.
2. **Finetuned gpt-neo 1.3b**: Fine-tuned on a conversational dataset (from Hugging Face) to learn how to interact with humans. It was then fine-tuned on a dataset containing both ambiguous and normal prompts, with examples of correct responses and guidance on how to ask clarification questions when faced with ambiguity.
3. **Self-refinement** - Iteratively improves responses by self-review, NLI evaluation, and refinement for enhanced coherence and quality.
4. **Result**: As a result, the model is now capable of engaging in conversations with humans and requesting clarification when needed. It is not perfect because of weakness of model and lack of dataset for finetuning model.

## Dataset
1. **Wikipedia dataset**: A large set of text data from Wikipedia articles was used for initial training of the GPT-1 model.
2. **Dialogue dataset**: I took dataset called "Anthropic HH (Harmless and Helpful) Golden" from hugging face
3. **User prompt+clarification dataset**: Using prompt engineering, I built a custom dataset for fine-tuning GPT-Neo. The dataset contains examples of unclear or ambiguous user prompts paired with appropriate clarification questions. It is structured with fields like label, prompt, and response. [dataset](./dataset.json)


## Code
1. In **gpt_finetuning1.ipynb** you can find code of finetuning of gpt-neo on conversational dataset ("Anthropic_HH_Golden" - with about 10000 examples). Weights of the model is here: https://drive.google.com/file/d/1MWM8_AMmPwngpE5_F_5gNvDh0lqbLGks/view?usp=sharing
2. In **gpt_finetuning2.ipynb** you can find code of finetuning of already finetuned model on dataset with unclear question. Weights of the finetuned model are here: https://drive.google.com/file/d/1AuYDz0VsbhjAc2BIqN6NvhJNz-WtSc8l/view?usp=sharing

