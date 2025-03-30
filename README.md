# StorySpark AI (Working Title)

## Project Overview

StorySpark AI is a personal project aimed at creating a streamlined web application that allows users, initially focused on my daughter, to collaboratively create interactive "choose your own adventure" style stories with an AI. Inspired by her love for audiobooks and detective stories (like Enid Blyton's "Famous Five" or "Die drei ???"), this app empowers her to define basic story parameters and then guide the narrative through choices, resulting in a unique story co-created with an AI assistant (like Claude or Gemini).

The core goal is to make story creation simple, engaging, and child-friendly. Completed stories can be read directly, listened to as automatically generated audiobooks (using Text-to-Speech like ElevenLabs), and eventually, illustrated with AI-generated images and even printed as physical books via Print-on-Demand services.

## Core Features (Planned & In Development)

*   **AI-Powered Story Generation:** Leverages Large Language Models (LLMs) to write story segments based on user parameters and choices.
*   **Interactive Choices:** Presents meaningful decision points allowing the user to shape the narrative path.
*   **"Series" Framework:** Enables defining recurring characters (like the user and her friends), settings, and themes (e.g., "Girl Detective Gang") for creating episodic stories within a persistent world.
*   **Text-to-Speech Audiobooks:** Automatically generates audio versions of completed stories using APIs like ElevenLabs.
*   **(Future) AI Image Generation:** Creates illustrations for story chapters/scenes.
*   **(Future) Print-on-Demand:** Option to order physical copies of the created storybooks.
*   **(Future) Web Interface:** Simple and intuitive UI with "Create," "Read," and "Listen" sections, including a visual "Bookshelf" for created stories.
*   **(Future) Marketplace:** Potential long-term goal to allow users to share and discover stories created by others.

## Technology Stack (Planned)

*   **Backend:** Python (using Flask/FastAPI TBD)
*   **AI Story Engine:** LLM API (e.g., Anthropic Claude, Google Gemini)
*   **AI Text-to-Speech:** TTS API (e.g., ElevenLabs)
*   **AI Image Generation:** Image Gen API (e.g., OpenAI DALL-E, Stability AI)
*   **Initial Data Storage:** JSON files
*   **Future Data Storage:** Pocketbase or PostgreSQL (TBD)
*   **Frontend:** HTML, CSS, JavaScript (Framework TBD)
*   **(Future) Print-on-Demand:** POD Provider API (e.g., Lulu, Printful)

## Current Status

The project is in the **early development stage (Phase 0-1)**, focusing on validating the core mechanics via a **Command Line Interface (CLI)** first.

**Current Focus:**
*   Setting up the basic project structure.
*   Implementing the core interactive text generation loop (LLM call -> display text -> display choices -> get user input -> repeat).
*   Saving story progress to JSON files.

See [PLANNING.md](PLANNING.md) for the detailed development roadmap.

## Getting Started (CLI - Phase 0/1)

*(This section will evolve as development progresses)*

**Prerequisites:**
*   Python 3.x installed
*   API Keys for the chosen LLM and TTS provider (set as environment variables or in a `.env` file)
*   Install dependencies: `pip install -r requirements.txt`

**Example Usage (Conceptual):**

```bash
# List available story series
python story_cli.py --list-series

# Create a new story within a series
python story_cli.py --series "GirlDetectives"

# (The script will then guide through the interactive creation process)

# Generate audio for a completed story (example)
python generate_audio.py --story-file "story_GirlDetectives_1678886400.json"