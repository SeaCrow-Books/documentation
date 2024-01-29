This is our current thinking in regards to creating prompts.
## Best Practice
[OpenAi's documentation on best practice](https://platform.openai.com/docs/guides/prompt-engineering/six-strategies-for-getting-better-results)

- If outputs are too long, ask for brief replies. 
- If outputs are too simple, ask for expert-level writing. 
- If you dislike the format, demonstrate the format you’d like to see. 
- Write clear instructions:
	- Include details in your query to get the more relevant answers. e.g. *Summarize the meeting notes in a single paragraph. Then write a markdown list of the speakers and each of their key points. Finally, list the next steps or action items suggested by the speakers, if any.*
	- Ask the model to adopt a persona. e.g. *Write in the style of Stephen King* 
	- Use delimiters to clearly indicate the distinct parts of the input. e.g. *\<section>This is a section\</section> or Title: This is a title*
	- Specify the steps required to complete a task, e.g. *Step 1:' this is the first step'* 
	- Provide examples
	- Split complex tasks into subtasks
	- Use classification to show importance. e.g. *This category with these sub-categories* 
	- Instruct the model to formulate its own solution in a stepwsie process before presenting a conclusion.
	- Tell the model to take a moment to think. Consider the [ReAct Framework](https://www.promptingguide.ai/techniques/react)

		<iframe width="560" height="315" src="https://www.youtube.com/embed/Eug2clsLtFs?si=w2TVOtMrr1KquJ1j" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

	- Ask the model if it misses anything in the previous response.
	- Tell the model to look at external sources. e.g. *websites*
- Test changes to prompts systemically. 

## Example Prompts

You will be presented with a news article. Your tasks is to identify any opinions expressed about the government, and their sentiment. 

Approach this task step-by-step, take your time and do not skip steps.

1. Read a paragraph of the news article.
2. Determine whether an opinion is express in this paragraph, if not, continue to the next paragraph. 
3. If there is an opinion, extract a JSON.
## Resources
[Great overview from open AI](https://www.youtube.com/watch?v=ahnGLM-RC1Y)

<iframe width="560" height="315" src="https://www.youtube.com/embed/ahnGLM-RC1Y?si=2ZFiDQqMw3NUfE0O" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


