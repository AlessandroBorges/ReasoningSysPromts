
# Reasoning System Prompts Promts
Reasoning System Promts for Small and Large Language Models (SLM/LLM)

For an didatic overview, check our article at Medium [Unlocking Reasoning on Small Language Models](https://medium.com/@alessandroborges_84477/unlocking-reasoning-on-small-language-models-f48ce438f1fa).



### Optimizing SLM Performance - Prompts and Inference Parameters
To achieve reasoning capabilities on SLM/LLM similar to a larger models, several technical considerations are crucial:

1. **Specialized System Prompts**
   
   SMLs perform best with focused, task-specific prompts due to their limited context window. For specialized tasks, craft reasoning prompts that target the specific domain and experiment iteratively to find optimal prompt structures. This targeted approach helps the model maintain focus and deliver more reliable results.

3. **Instruction-Tuned Models**
   
   Choose models specifically trained to follow instructions, as they're better equipped to execute structured reasoning steps defined in system prompts. Models like Phi-3-mini-instruct and Llama 3.2 3B instruct excel in this aspect.

5. **Temperature Control**
   
   Lower temperature settings (0.35-0.45) help maintain focus on structured reasoning. While higher temperatures can promote creative thinking, they may cause SLMs to deviate from prescribed instruction paths.

7. **Repetition Penalty Management**
   
   Many inference tools apply a default repetition penalty of 1.10. For reasoning tasks, this can be counterproductive as the structured thinking process inherently involves repetitive patterns. Consider disabling or minimizing this parameter to avoid disrupting the model's reasoning flow.

## Crafting Reasoning System Prompts

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

Verification Framework tips - You can include explicit verification steps to ensure reliability, like:

    Solution consistency check
    Assumption validation
    Edge case consideration
    Logic verification

    Example Implementation (Optional) - Providing a concrete example helps the model understand the expected reasoning pattern. Make it:

    Concise but complete
    Relevant to the task domain
    Clear in demonstrating the reasoning process

### Disclaimer

The techniques presented in this article demonstrate potential approaches for enhancing reasoning capabilities in Small Language Models (SLMs). While models like Phi-3-mini and Meta's Llama 3.2 3B have shown promising results with these methods, performance can vary significantly across different models, tasks, and implementations.

Please note:

    Results may not be consistent or reliable across all SLMs
    Performance can vary between different versions of the same model family
    Success rates depend heavily on proper prompt engineering and parameter tuning
    These techniques require thorough testing and validation for specific use cases

Users should conduct their own comprehensive evaluation and testing before implementing these approaches in production environments. The methods described here are experimental and should be used with appropriate consideration of their limitations and potential risks.

This article is intended for educational and research purposes only. The author makes no warranties or guarantees regarding the effectiveness, reliability, or suitability of these techniques for any specific application.

