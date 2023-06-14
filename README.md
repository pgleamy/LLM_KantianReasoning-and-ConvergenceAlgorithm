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