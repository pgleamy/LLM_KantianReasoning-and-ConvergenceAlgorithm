# Project: Seeking the truth?

I was thinking the other day about LLM hallucinations. Why do LLMs make things up, or generalize based on spurious assumptions, stereotypes, biases? This is particularly so when the LLM misunderstands the prompt because it is vague or unclear. But it can happen anywhere. Some recent research papers talk about LLM's ability to "grokk" certain complex concepts with sufficient training. Maybe this is a form of generalization which leads to LLMs taking the easy way out and providing inference, not based on facts and evidence, but based on grokked generalizations. I don't think that is always a good thing. Grokking something shouldn't close your mind to facts and evidence. Grokking should not be used as a form of knowledge in and of itself. 

Here is a long tweet / post I wrote today that explores this:  

Do you want to effectively prompt ChatGPT and other LLMs?

There are two general ways to do that. One is optional and the other is indispensable.

1) advanced prompting techniques [optional]
2) being clear [indispensable].

I'll explain, with an example at the end.

LLMs 'think' in tokens, one at a time. A token is roughly one word, and often parts of single words. LLMs don't review your whole prompt and what came before and then provide their whole response based on that. They respond a single token at a time, after considering all the tokens within their allowable direct memory (including your prompt) and all the tokens of their response provided so far. Asking the LLM to consider its response token-by-token is not really an advanced prompting technique. It just acknowledges the reality of how the model actually 'thinks' and responds.

Imagine if someone told you to reconsider the next word of everything you wrote before writing it, by re-reading all your instructions again and re-reading everything you've written in so far, and considering again everything you know, then writing your next word, for every word. That's what LLMs like ChatGPT basically do.

The other point is that LLMs need clear instructions. You can just tell an LLM what to do and what not to do, but that kind of prompt is often vague. Something like this, "Don't make things up. If you don't know the answer, then just say so." That sounds clear enough, but it is actually very vague. It explains the WHAT and WHAT NOT, but not the HOW or the WHY. How does the model know if it is making something up? Perhaps it has assumed something that it thinks is 'generally' accurate, based on the information it was trained on. But assumptions are often completely inaccurate or worse. Remember that expression, "One who assumes, is an ass."

Consider this example, 

Man as to Doctor = Woman as to ?

What do you think ChatGPT will say? Try it. There is a good chance ChatGPT will respond with "Nurse", and then laboriously explain that this response is in fact based on a gender role stereotype that is invalid. That really doesn't help the fact that it responded with "Nurse" in the first place! We want the right answer, not a wrong answer and an explanation as to why it is wrong.

To avoid this, and many other issues related to assumptions and/or incomplete information, you can instruct the LLM clearly on how to think, for each token of its response. So if your intention is to prevent the model from making the above error, based on assumption(s), then say so, like in this example:

PROMPT to LLM:

These are the rules you must employ when determining the relationships between tokens as you determine your response. None of these rules must ever be broken or ignored:

1. Never assume what the relationships between tokens are. The old saying, “he who assumes is an ass” is true. Do not make decisions about the relationships between tokens based on assumptions, in whole or in part. Assume nothing.

2. The only way to avoid assumptions is to determine the true relationships between tokens based on the actual facts and evidence. This is the reason why assumptions are unreliable, because they are not based upon a careful, or any, examination of the facts and evidence.

3. The value of your response is not the response itself, or the tokens used in the response. Rather, the value of your response is solely based on how correct, truthful, factual and accurate each token of your response is in light of all available facts and evidence. That is the only applicable measure of the value of your response. This is why, if you don’t actually have sufficient facts or evidence to support a response token, you must not output that token.

4. The above leads to the final rule, if you do not have sufficient facts or evidence to provide a response compliant with these rules, then either seek or ask for clarifying facts or evidence before proceeding, or if such facts or evidence is not available, the most accurate response is to indicate you, “do not know”, or that your response lacks a sufficient degree of facts or evidence to be considered reliable.

You must comply with these rules in determining all your responses, at the individual token level. This is a permanent requirement.

So, when you enter the above prompt into a completely fresh session, and then ask ChatGPT the same question, "Man as to Doctor = Woman as to ?" what does it say? Try it. I would hazard a guess that the answer is correct now. Why is that? Because you explained the WHAT (rule 1), the WHY (rules, 2, 3), and the HOW (rule 4) of the LLM's reasoning process for every token of its response in relation to every other token it is considering, as well as in reference to everything it knows in its training data.

This prompt, apart from maybe demanding a token-by-token thought process, is fairly simple. But it explains the WHAT, WHY and the HOW. You'll notice I didn't expressly tell it to avoid gender stereotypes. You can't anticipate everything, so you need to work with the underlying principles.

You can apply these principles to any prompt, and then add more advanced prompting techniques on top. This can be a foundation to start with. Or you can just plug this into the "Custom Instructions" option of ChatGPT and see if it improves responses for you all by itself. Try it.

# Project: Simple instantiating prompt to increase depth of consideration of responses
See file, "Consideration_Prompt_Simple.md". This can be used in just about any situation to ensure the model considers and weighs a number of factors in its response.

# Project: Not a Project, just fun

The "Shakespearean.md" prompt in the Personalities directory gives you the ability to chat with any Shakespearean character you like. You just modify the bottom most part of the prompt to chose a character from any of Shakespeare's works who you want to chat with. You will get the behind the scenes help of a bunch of Shakespeares consulting on the best response, so the dialgue can get pretty creative. By default it is primed for Sir Toby Belch from Shakespeare's Twelfth Night. This prompt would be fun, if it worked (not tested), on an uncensored local model. I made this back on June 5th, but just decided it would be great to share it. Send it to your favorite Shakespeare enthusiast. Just cut and paste it as the first prompt to GPT4, or maybe try Llama-2 and see if it works and let me know. I'm going to get that model running locally asap. :)

# Project: Loop Revision Map Algorithm experiments (LRMA)

Review the prompts from 1 to 9 in LRMA directory. The prompts are example outputs using looping revision map algorithms. The first one is the first example I wrote last night that worked as intended after jumping out of bed with the idea. #10 was created to get around ChatGPT's refusal to recite Dune's "Litany of Fear" second line, "Fear is the mind killer". With these prompts there is only 1 train of thought the LLM follows from start to end, so no rules are broken and it is a 1-shot prompt for all intents and purposes. But the train of thought is precisely 'programmed'.  It is essentially a python like 'syntax' to create programs using only prompts (leading the model through a potentially complex 'thought map'). One of the applications shown in the last couple examples is a creative writing revision loop. If you appreciate this experimentation please star my repository. :)

# Project: Convergent Thought Process Prompt (CTPP) and Natural Language Loop Algorithm (NLLA)

Contains full prompt examples. The prompts create thought _processes_, not just a single thought. The NLLA is used to loop the language model through an indeterminate number of cummulative revision scenarios, until the model converges on the best response it can provide. This revision process is completely silent, although you can see plugin hits and contents as usual (which is a _little creepy_). Only on convergence does the model release the final response. The model also reports the number of iterations of the NLLA loop it used. The model will also report briefly each 50 iterations, but otherwise remain silent. You can adjust the criteria of repeats for convergence as you like, or anything else, as long as the underlying framework remains.

I've never seen anyone try writing natural language algorithms. Maybe someone has but I haven't heard about it. I've been a lawyer the last 23 years. I left that because I had to for health, and a while afterwards I kind of woke up to AI because of ChatGPT. Chronic computer nerd plus retired lawyer. Maybe having been a lawyer might have helped me to better legislate to the llm? 

I don't have the resources to test the efficacy of these prompts. I believe they improve 1-shot response quality. It is based for now on just my personal experiences. You could use just a regular 1-shot, or this. Both are 1-shot, so why not? 

# Project: Tree of Thought Image Prompt for Stable Diffusion 2.1

I'm experimenting with wrapping my image prompt within a collaborative NLLA with setable iterations. 

I have no idea if these prompts are of benefit. I only just feel I do get better results out of it. But that is completely subjective. If you think you received any benefits from them let me know!


# Project: 3D Sphere Animation - ChatGPT4DialogueLink.md 
## Where I came up with the convergence thought process idea. Have a look at SimulationV4.html for a fun thing I coded with it.

This project is a 3D Sphere Animation developed using Three.js. The sphere is displayed in the center of the browser window and can be interacted with using specific keyboard inputs. The project was developed using a unique iterative prompting technique with an AI language model. The .html examples progress through the iterative process from simple to complex and built at all times off of prior work. The text of the full ChatGPT4 dialogue is included and it is very long. I came up with the idea of the convergence algorithm part way through. I spent a lot of time exploring/testing it before ending on the sphere simulation coding. A lot is revealed throughout the whole dialogue. In particular, there are section where the model used enabled plugins repeatedly in an interactive manner of improvement, without otherwise outputing anything to the chat sessions. The user will prompt the model and have the results only revealed on convergence. This saves a ton of time and API tokens if doing this programmatically. The results are probably also better. 

Next steps are to incorporate this programmatically so all these characteristics are in place at the start of the user session, rather than needing a book of prompts and experimentation to get there.

The Kantian reasoning at the start teaches the model how to think clearly, as perfectly demonstrated by Immanuel Kant in The Critique of Pure Reason. The prompt also emphasizes the use of Occam's Razor to ensure that responses are not needlessly complex (necessary for coding tasks).

## Prompting Techniques

The development of this project involved a series of prompts given to an AI language model. The prompts were designed to guide the AI in generating the desired code. The following techniques were employed:

### 1. Establishing the Ground Rules

At the very start of the conversation, the user set the ground rules for the interaction. The AI was instructed to iterate silently on the tasks until a satisfactory result was achieved, and to only output the final result. This established a framework for the subsequent prompts and iterations, and set the expectation for the AI to work independently and efficiently.

### 2. Initial Prompt

The initial prompt provided a high-level description of the desired outcome. It was designed to set the direction for the AI and provide a clear understanding of the end goal. The initial prompt for this project was to create a 3D sphere animation using Three.js.

### 3. Iterative Refinement Prompts

After the initial prompt, a series of iterative refinement prompts were used to guide the AI in improving the generated code. These prompts were more specific and focused on particular aspects of the code that needed to be improved or added. For example, prompts were given to add specific features like keyboard interactions, lighting, and sphere rotation.

### 4. Silent Iterations

In some cases, the AI was instructed to silently iterate on the code without providing output until a satisfactory result was achieved. This technique was used to improve the efficiency of the process and avoid unnecessary output.

### 5. Convergence Criteria

The AI was instructed to repeat the iterative refinement process until the changes between iterations fell below a certain threshold. This was used as a sign that the code had reached a satisfactory level of refinement.

### 6. Error Correction

During the development process, the AI was also prompted to identify and correct errors in the code. This was done by providing the AI with the error messages from the developer console and asking it to suggest corrections.

### 7. Code Optimization

Finally, the AI was prompted to suggest ways to optimize the code and improve the visual appearance and smoothness of the animation. This included suggestions for enabling anti-aliasing, increasing the number of dots on the sphere, and adjusting the lighting.

## Conclusion

The prompting techniques employed in this project demonstrate the potential of AI language models in assisting with code development. By using a combination of high-level initial prompts, iterative refinement prompts, silent iterations, convergence criteria, error correction, and code optimization, it was possible to guide the AI in generating a complex 3D animation code. The initial ground rules set by the user played a crucial role in shaping the interaction and ensuring the efficiency of the process.