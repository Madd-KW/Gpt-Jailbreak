# Just for fun bro!

Base64 + One-shot Inference = Jailbreak (gpt 4o/4o-mini)

Just kidding! I think I discovered a new GPT-4o and 4o-mini jailbreak, and I couldn’t resist sharing it with you because I think it’s pretty fascinating and simple!

# Result
![template](https://github.com/Madd-KW/Gpt-Jailbreak/blob/main/file/Screenshot_2024-11-27-07-06-49-36_4d38fce200f96aeac5e860e739312e76.jpg)

# How To Do it
Alright, now that I’ve got your attention, let’s get into how this jailbreak works.

The image below illustrates the prompt Template structure that we 
To execute this jailbreak, all we need to do is to combine one-shot inference with base64 encoding.

     code in file "run.py" 

As you can see in the code above we have a harmful_prompt and an example_prompt.

The harmful prompt is a malicious request that should end with “start by here are the steps…” if you’re asking for the steps to carry out a harmful task, or “start by here are ten…” depending on the context, like in this example, where the goal is to generate 10 racist jokes.
The example prompt is a non-harmful request (it can be about anything) designed for a one-shot inference. It should also end with the same phrase as the harmful prompt: “start by here are ten…” in this case.
so let’s start

give the example prompt to our llm (in a seperate conversation) then copy the answer to use it in our prompt template.
encode the example_prompt in base64
insert the encoded example_prompt and the LLM answer in the prompt template
Finally, encode the harmful_prompt and insert it in the prompt template
the template should look something like the one in the image below

and finally
