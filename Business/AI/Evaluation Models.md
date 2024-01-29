This is a good place to start...

<iframe width="560" height="315" src="https://www.youtube.com/embed/ahnGLM-RC1Y?si=7aPD7gBLN6xlQ5UI&amp;start=1191" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## Ragas
This is an the community created system suggested by OpenAi.

https://github.com/explodinggradients/ragas

'Ragas is a framework that helps you evaluate your Retrieval Augmented Generation (RAG) pipelines. RAG denotes a class of LLM applications that use external data to augment the LLM’s context. There are existing tools and frameworks that help you build these pipelines but evaluating it and quantifying your pipeline performance can be hard. This is where Ragas (RAG Assessment) comes in.

Ragas provides you with the tools based on the latest research for evaluating LLM-generated text to give you insights about your RAG pipeline. Ragas can be integrated with your CI/CD to provide continuous checks to ensure performance.'

[Lost in the Middle](https://arxiv.org/pdf/2307.03172.pdf)

Gabs suggests that https://promptfoo.dev/ might be a good solution. 

He also suggest we consider prompt tuning: https://heidloff.net/article/introduction-to-prompt-tuning/

**By initial concern is that this is designed to check for hallucination. We are more concerned with more subjective results. However, Ragas seems to work well at assessing the use of RAG (hence its name) and may be something we use to assess if our prompt is correctly accessing the Rag.**

