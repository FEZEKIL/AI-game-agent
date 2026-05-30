# Adaptive Pick-Your-Path Game with LangGraph
This project implements an AI-powered interactive storytelling engine using LangGraph, bringing classic "pick-your-path" adventure games to life. Players can type natural language inputs, and an intelligent agent interprets their intent to guide them through a branching narrative.

Project Description
The game allows players to shape the narrative by making choices at key moments. Instead of a fixed plot, the player is presented with a scene and can choose from a set of possible actions. The AI, powered by OpenAI's language models, interprets these choices and transitions the player to different scenes, leading to various outcomes and endings.

Technologies Used
LangChain: For building applications with large language models.
LangGraph: A library for building stateful, multi-actor applications with LLMs, used here to manage the game's state and transitions.
OpenAI: Provides the underlying large language model (gpt-5.4-nano) for interpreting player input.
Python: The core programming language.
Setup and Installation
To set up and run this project, follow these steps:

Install Dependencies: The project requires langchain-openai and langgraph. These are installed at the beginning of the notebook.

!pip install langchain_openai
OpenAI API Key: You need an OpenAI API key to use the language model. Set your API key in the environment variable OPENAI_API_KEY within the notebook:

import os
os.environ["OPENAI_API_KEY"] = "YOUR_OPENAI_API_KEY" # Replace with your actual OpenAI API Key
Important: Remember to replace "YOUR_OPENAI_API_KEY" with your actual OpenAI API key.

Run the Notebook Cells: Execute all the cells in the notebook sequentially. This will:

Define the game scenes (SCENES).
Define the game state (GameState).
Set up the render_scene, interpret_action, transition, and check_end functions.
Construct the LangGraph workflow.
Initialize and compile the game.
How to Play
Once all the cells are executed, the run_game() function at the end of the notebook will start the game. You will be presented with the first scene, and then prompted to enter your actions. The game will interpret your input and guide you through the story until an ending is reached.

Example gameplay:

==================================================
Your alarm goes off at 7:00 AM. Today is the day of your big group presentation in Professor Mendel's class — the one worth 40% of your grade. You have one hour before you need to leave. You're a little nervous, so maybe you should rehearse, but you're also hungry so you could make breakfast. Or maybe you should just go early and get it over with.

What do you do?

> rehearse
==================================================
You stand in front of the mirror, running through your section. Halfway through, you catch something — slide 4 says 'financial forecats' instead of 'forecasts.' Yikes.

What do you do?

> fix the typo
==================================================
You walk into the lecture hall feeling unusually prepared. The rest of your group is huddled near the podium and they look relieved to see you. Professor Mendel asks who wants to go first.

What do you do?

> I'll go first
==================================================
ENDING — Standing Ovation. You nail it. Your group lights up, the class actually claps, and Professor Mendel nods the slow nod that means an A. Your groupmate Priya buys you a coffee on the way out. Roll credits.

Game Over.
Enjoy the adventure!
