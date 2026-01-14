# Travel Location Content Automation — Grounded LLM Pipeline

This repository contains a pipeline for generating high-quality travel location content (stations, neighbourhoods, areas) using LLMs without hallucination.
The project is intentionally opinionated: it treats LLMs as probabilistic writers, not truth engines, and builds guardrails around that assumption.

Most LLM-based content systems fail in one of two ways:  
They hallucinate details confidently.  
They avoid hallucination by becoming generic and useless.  

Core Design Principles  
This repository is built around a few non-negotiable principles:  

1. Separate research from writing  
The model that searches the web is not the model that writes prose.  

2. Ground first, generate later  
All generation is constrained to an explicit factual context.  

3. Surface uncertainty explicitly  
Missing information is shown as [[UNKNOWN: ...]], not hidden or smoothed over.  

4. Structure before style  
Content structure is fixed and validated before tone is applied.  

5. LLMs propose; systems verify  
Every generated article is checked against its source context.  

