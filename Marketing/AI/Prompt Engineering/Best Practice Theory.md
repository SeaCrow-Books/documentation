Everyone has their own approach to Prompt engineering, resulting in different levels of success and, more importantly, consistency.

At SeaCrow we tend to look at how [LLMs](https://en.wikipedia.org/wiki/Large_language_model) and other AI tools are created to then decide what the best approaches, workflows, and prompts are when creating content. 

We also believe that our post writing workflow should mirror our prompt engineering approach to ensure consistency in output but also to train employees in how to think when generating content across the board.

>[!Note]
>If you have a different approach, philosophy, or thought process on how a specific AI tool should be used, then please share it. AI is a growing and rapidly changing technology, its essential we remain at the forefront of understanding. 
>
>We're not so arrogant to think we understand everything about AI. 

With that in mind, let's explore our approach.

# Neural Network Structures

The internet is riddled with explanations, I'm not going to break it down here. But there are three things about [Neural Networks](https://en.wikipedia.org/wiki/Neural_network#:~:text=A%20neural%20network%20is%20a,a%20feedforward%20artificial%20neural%20network) that you need to always keep in mind.

## 1. Synapses: Everything is interlinked

Large Language Models (LLM) like Chat GPT are created on enormous datasets. What makes them so powerful is that they're built on the structure of a Neural Network, like your brain. So individual data points aren't just floating around, waiting to be searched. The data points are all interconnected with one another, and you can tell an LLM to make a prediction, connection, or inference based on how these points are connected.

What that means practically, especially with regards to writing posts, is that you can tell Chat GPT to make connections or comment on trends between genres, tropes, current popular genre subversions, overlaps and fusions between subgenres, reader reception/popularity, influences from other genres, and cultural impacts. It knows all of this (to some degree) because this information is somewhere on the internet, meaning it's somewhere in its dataset.

*The Big Take-Away: When writing about a certain topic, don't limit yourself and the reasoning/discussions in the blog post to one "synapse", you want to leverage as many **relevant** data points as possible so that the generated text mimics the insight and knowledge of an expert.*

With our toning, writing style techniques, and randomization clauses painted over this "expert insight", it makes our blog posts more relatable, less shallow, and more human. 

___Information is one thing, but insight is everything.___

## 2. Memory Loss and Miscommunication

### There are two sides to this.
On a larger scale, LLM chat rooms, like the conversation room of Chat GPT, have literal memory limits. It will struggle to keep an overall context snapshot, or follow a logical progression from point to point, if your chat becomes too long. Which is literally why you can't write a full book in a chat.

On a more granular level, and more relevant to writing blogposts and our workflow, it will forget what you want to prioritize in your project and deviate from your end goal if you are not giving it explicit, structured, and unambiguous instructions. 

### What does this look like?
Well take this scenario for example:

- You give GPT a well thought out Context Prompt and an explicit list of instructions. 
- You then add a clause like "please recommend additional relevant elements I might want to focus on".
- GPT gives a few a good answers or bad ones. 
- You then tell it to "include this one and this one".
- And then you start working on an extremely long blog post.

This seems like a good workflow, but after a lot of generated text you'll inevitably notice that it's excluding some of your listed elements/categories/instructions.

The reason for this is it can't remember which of the two "instruction sets" were more important. Your highly detailed and well thought out Context prompt, or the tiny "yeah, include this one and this one" prompt.

Additionally, if you don't explicitly tell it to not include some of the elements it suggested that you didn't want to include, it will inevitably start slipping those suckers in. **Which means consistency has gone out the window.**

Sometimes Chat GPT is kind and you can circumvent the issue with a few well-worded prompts, but the point is you might not always realize a problem is creeping in. And sometimes Chat is just an ass. That's why we have a very specific workflow that doesn't allow this issue to creep in. 

You can see a specific workflow for all blog posts outlined in the [[!AI Best Practices for Blog Posts]] document for a breakdown of this process. But I will include a more generalized prompt engineering one below.
## 3. Weighted Terms:

No matter how well you word and structure a prompt, or how many hours you spend crafting the "perfect prompt", there are a few wildcard terms that can completely override your efforts. ___This is a bit more relevant to Midjourney, but GPT has a few quirks too.___

Explaining this with Midjourney in mind is a lot easier, but the concept applies to GPT as well (if to a lesser extent).

I mentioned above that Neural Network AI models are created on large datasets, well not all datasets are created equally. Let's explain. Digital artists love drawing dragons, but I assume very few of them out there are drawing walruses. This means that Midjourney has a bigger data set of dragons drawn in thousands of different styles than it does of walruses.

You might think "That's great, a dragon will be easy to create". Well yes, but the term "dragon" is loaded with so much context that Midjourney will basically ignore whatever else you add to your prompt, making generating a complex scene with things interacting with that dragon very difficult.

Whereas it has a general idea of what a walrus looks like, so whatever additional information you give it will carry more "weight" to the overall composition of the image.

(There are very complex parameters that enable you to lower and raise the weight of a term or gain other granular controls over the output of an image, but you don't always have a day to spend on tweaking a prompt for a single image.)

Another actual example is the almost comical inability for Midjourney to create a barefooted Viking, since all the images of "Vikings" it was trained on were wearing boots. So it can't separate the idea of "boots" away from the term "Viking". 

The thing to remember is that midjounrey 

Improvements are made to these models every day, eliminating the effects of these "weighted terms" and other random idiosyncrasies. But it's good practice to always consider what the actual dataset of a topic probably looked like if you're struggling with generating content for a certain concept. 

With Chat GPT these types of weighted terms are less "visual", but there are enough articles out there that say GPT-generated content is full of stereotypes or generalizations. Unfortunately, there's so much of it on the internet that it affects the bigger data set.

# Prompt Engineering Best Practices

We circumvent most of these problems and ensure consistency across our content through two main concepts:

### 1. Granular control over output through hyper-specific prompts (and custom instructions).

Gaining granular control over output is basically achieved through a trial and error process where you try to identify every single factor/variable that might affect your desired outcome and then creating rules to either control those factors/variables or exclude them from the dataset.

This is mostly used to gain control over the tone, voice, and prose of text in GPT. And of course to tell it exactly what you want it to do.

Eventually, we'll gain access to the API and Fine Tune this control even further.

### 2. Isolated Workflow Stages (our #Golden-Rule)

When working with long chats in GPT, your main struggle is going to be to get it to remain consistent and remember all the context in sequential order. This is true for writing blog posts of course, but it is also true if you are busy developing a prompt tool or any kind of robust template/outline that you want to recycle a lot.

The following workflow structure helps to address this issue:

#### 2.1. Planning (Down the Rabbit Hole)

When designing a prompt, outline, or eliciting certain information out of GPT, you don't always have a full picture/idea of what you want, or even know anything about a subject. When this is the case, and even when you don't think it is, it's a good idea to mess around in Chat GPT and ask as many questions as possible.

As you start building a bigger knowledge base, or understand the nature of your problem better, you'll realize what kind of questions you should really be asking. And if you hit a wall, just ask Chat what other concepts related to your topic you haven't explored yet and then go down more Rabbit Holes. The only caveat being, you don't have unlimited time so be purposeful about what kind of sub-topics/adjacent synapses you are exploring.

### 2.2. Summarizing and Structuring

Once you have a fleshed out knowledgebase from which to work, it's a good idea to condense and structure everything you and Chat have explored together.

When condensing the information and summarizing it, you'll notice one key thing. 

___Chat makes shit up.___ 

It loves lying, so double check the information (it's getting a bit better at not lying, but just stay wary). This is know as [hallucination](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)). But even when it's not outright lying, you'll notice that it may mention certain concepts under different names/terms and if you categorize stuff, it will even list those terms under different categories. So while it's great at producing a lot of excellent information, it's largely up to you to spot errors, repetitions, and incorrectly categorized items.

After you've fixed the structure of your information, always tell Chat what you did. It needs to learn to get better, so do your part. You can even ask it if you did something wrong, or if it can spot other problems and you can fix that together.

It is always a good tactic to ask Chat if the information it is providing is incorrect, if it has missed anything important, or, even, what it should include that you have not included. Chat knows everything but will not always tell you unless you ask directly. 

Structure types:

- If you're building a prompt, this is also the step where you structure the prompt in such a way that it covers all the bases and excludes all variables you don't want to have affecting your output.
- If you're building a template, this is the step to cement its structure.
- And finally, if you're writing a post, now is the time to cement your outline. You should NOT be including phrases like "suggest more aspects to the structure" -- you should have done that already by now.

>[!important]
>- You need to end this stage with your Context Prompt. 
>- You will either start a new chat where you paste your perfectly crafted Context Prompt and Outline (preferred), or you will explicitly tell Chat something along the lines of "Keep the context of our chat in mind, but only follow instructions from this point on, placing a greater priority on the following Context Prompt. 
> - - Only use the second option when dealing with a very complex issue and Chat will benefit from the established context.
>- This is also the step where you prime the tone of the generated text, both by pasting in the custom instructions, and by using the [[Post Toning]] trick.

### 2.3. Execution

This will look different depending on what tool/prompt you created. For most use cases, this is where you test your tool, go back through steps 1 and 2, and finalize it -- or use it for whatever you created it.

With regards to writing blogs, this is where you and Chat GPT generate each section/segment of your post step-by-step (which you have already outlined in the previous section).ction).

You will largely make use of our finalized prompts to generate the majority of the content, like the [[Subgenre and Trope Prompts for Pillar Posts]].

However, you will also use generic prompts to tweak the content, like:

- Give me three iterations/alternatives for this section.
- I don't like (this) imagery, give me alternatives.
- I don't agree with (this) statement, let's explore (this) thought/perspective instead.

>[!caution]
>You need to be really wary/vigilant of not accidentally overriding a style/tone element or accidentally undermining the structure/outline of your post when using generic prompts to tweak content.

Therefore, where possible, it's best to rely on well thought out and cemented prompts that we know won't clash with other elements or variables that we are trying to control.
So if you have a suggestion for a robust prompt that can cut down on the workflow or address a common issue, then please hop into Discord and we can chat about it. 

For the most part, we'll try to build outlines and supporting prompts/custom instructions that will streamline this workflow and circumvent common issues. The whole point of our system is to not spend days struggling to write a blog post.
### 2.4. Edit

AI will only get you so far, and we value individualism. So if you want, edit the living daylights out of a post ==just ensure it still reflects the tone of the blog author==. But otherwise, just make sure it didn't generate any offensive phrases and try to cut out as much cringe as possible (an unfortunate side-effect of our toned custom instructions).


# Conclusion

So the main things to remember are:
1. Try to harness as many synapses/datasets as possible while remaining relevant.
2. Chat GPT will lie, forget, and purposefully lead you astray. Love her, but never trust her.
3. Midjourney is a bigot and has a fascination with wonky hands, do your best to mitigate it.
4. Remember to Compartmentalize/Segregate/Sever (whatever adjective you want to use) the different steps in the prompt engineering and, by extension, the blog writing workflow.
5. Create Master Prompts for controlling and eliminating variables when necessary.


