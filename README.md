# Context-Verified RAG System for PDF Analysis
This project is a localized RAG application designed to process PDF documents and verify whether LLM-generated answers are strcitly grounded in the source text or contains hallucinations.

It uses LLM in two roles:
## Generator - generates answer
## Evaluator (LLM-as-a-Judge) - reviews answer and generates confidence score

The system provides confidence score and structural label to every response generated-

**0.8-1.0 (Grounded)**- The answer is directly verified and supported by document.
**0.4-0.79 (Partially Grounded)**- The answer contains facts with imprecise context.
**0.0-0.39 (Hallucinated)**- The query is outside the source document scope.
