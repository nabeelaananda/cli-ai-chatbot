# CLI AI Chatbot

A simple Command-Line Interface (CLI) chatbot built with Python that interacts with an AI API. This is my 8th learning project, focusing on API integration and continuous user interaction in the terminal.

## Features
- **Continuous Chat:** Maintains conversation context (memory) using thread IDs, allowing the AI to remember previous messages in the session.
- **Thread Reset:** Built-in `new` command to instantly clear the conversation context and start a fresh thread.
- **Secure Credentials:** Uses environment variables to securely load the API key without hardcoding it into the script.

## Prerequisites
- Python 3.x
- `requests` library (`pip install requests`)
- A valid API Key stored as an environment variable named `MIMO_OPENAI_API_KEY`.

## How to Run
1. Clone this repository to your local machine.
2. Ensure you have set the API key in your environment variables.
3. Run the script via terminal: `python chatbot.py`
4. Type your message and press Enter. Type `new` to reset the chat, or `exit` to quit the program.

## What I Learned
Through building this project, I gained practical experience in:
- **API Integration:** Using the `requests` library to send POST requests, pass headers, and parse JSON responses.
- **Security Best Practices:** Keeping sensitive information like API keys out of the source code using `os.getenv()`.
- **Control Flow:** Managing an infinite loop (`while True`) to continuously prompt for user input and handling specific string commands (`break`, `continue`).
- **State Management:** Storing and updating variables (like `thread_id`) to maintain the state of the conversation.

## Future Upgrades
To keep the core code clean for now, I plan to add the following features in future iterations:
- [ ] Add terminal color formatting (e.g., using `colorama`) to easily distinguish between User and AI messages.
- [ ] Implement robust error handling (e.g., `try-except` blocks) for network timeouts or invalid API keys.
- [ ] Add functionality to export or save the chat history locally into a `.txt` or `.md` file.
