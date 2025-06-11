# kipam - The AI based project manager 
KiPAM is an AI based project manager, which helps to structure and streamline the process of setting up and work on a new project based on the principles of the "passionate project planning" framework.

## How does it work?
It's using a chat bot with a highly detailed chat prompt, which you can find in the `prompts` directory. After each session, you'd have to execute the `update_life_context.py` script which is taking the latest chat history out of the `conversations` folder and puts all discussed details of the project into the `profiles/Project KiPAM Context.md` file, which will then be used during the next conversation. 


## Setup
This chapter describes how you can setup the chat bot

### Requirements
- This GitHub repository forked and cloned to your local hard drive
- Either
  - A working [Ollama](https://ollama.com/) instance
- Or
  - An API key for OpenAI / Anthropic AI
- [Obsidian Notebook](https://obsidian.md/) as chat bot
- Python 3


Just fork and clone this repository and make sure you're having a properly configured AI somewhere at hand. It runs with a locally installed `ollama` instance or with remote APIs to access OpenAI, Gemini and Anthropic AIs.

You need to have a working python environment in order to execute the python script. 

And you need to have an installed and configured version of [Obsidian Notebook](https://obsidian.md/) installed on your local system. Please also install the community plugin [BMO Chat Bot](https://www.obsidianstats.com/plugins/bmo-chatbot) into Obsidian. 


## Workflow
After you've set up Obsidian and the BMO Chatbot community plugin, you can start a new BMO Chat window and you can start your conversation with the AI prompt. 

Once you're done discussing your new project, just type `/save` in the chat window to save the chat protocol. 

Then execute the python script in order to update the current context file (which acts somehow as the brain and memory of your chat). Then you're able to continue the discussion. 

The chat bot should always remind you of the state of the project.


## Trials & Errors
This is the collection of trails & errors we found along our experiments:

Editor System Role in BMO settings need to be empty.
llama3.2 quality is insufficient
