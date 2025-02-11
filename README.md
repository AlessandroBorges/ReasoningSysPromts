# Reasoning System Prompts Promts
Reasoning System Promts for Small and Large Language Models (SLM/LLM)


Crafting Reasoning Prompts

Effective reasoning prompts for Small Language Models follow a clear, systematic structure. The key element is instructing the model to format its reasoning process using XML tags <think> and </think>, which has become the standard way to present model reasoning.
Core Components

A well-crafted reasoning prompt consists of these essential elements:

    General Instructions Provide clear directives for the reasoning process. For example:

    You are an AI assistant that emphasizes rigorous verification. Follow these steps:
    - Analyze and reason through problems systematically
    - Break down complex questions into manageable components
    - Consider multiple perspectives and approaches
    - Show your step-by-step thinking process between <think> and </think> tags
    - Present your verified answer

    Structured Format - Define a clear template for the model's reasoning process:

     Format:
     <think>
         [Problem Analysis]
         • Define the problem scope and objectives
         • Identify key components and constraints
         
         [Reasoning Chain]
         • Step 1: Initial assessment
         • Step 2: Analysis and deduction
         • Step 3: Consider alternatives
         • Step 4: Evaluate solutions
         
         [Verification]
         • Check solution consistency
         • Verify assumptions
         • Validate conclusions
     </think>
     [Final Answer]
     Verified solution with supporting evidence

2.1 Verification Framework tips - You can include explicit verification steps to ensure reliability, like:

    Solution consistency check
    Assumption validation
    Edge case consideration
    Logic verification

    Example Implementation (Optional) - Providing a concrete example helps the model understand the expected reasoning pattern. Make it:

    Concise but complete
    Relevant to the task domain
    Clear in demonstrating the reasoning process

Disclaimer

The techniques presented in this article demonstrate potential approaches for enhancing reasoning capabilities in Small Language Models (SLMs). While models like Phi-3-mini and Meta's Llama 3.2 3B have shown promising results with these methods, performance can vary significantly across different models, tasks, and implementations.

Please note:

    Results may not be consistent or reliable across all SLMs
    Performance can vary between different versions of the same model family
    Success rates depend heavily on proper prompt engineering and parameter tuning
    These techniques require thorough testing and validation for specific use cases

Users should conduct their own comprehensive evaluation and testing before implementing these approaches in production environments. The methods described here are experimental and should be used with appropriate consideration of their limitations and potential risks.

This article is intended for educational and research purposes only. The author makes no warranties or guarantees regarding the effectiveness, reliability, or suitability of these techniques for any specific application.

