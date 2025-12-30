# AI Chat Interfaces Project

This project consists of two standalone HTML-based chat interfaces for interacting with AI models:
- **Mini ChatGPT**: A simple web app for chatting with OpenAI's GPT models (e.g., GPT-4o-mini).
- **Gemini Chat**: A basic web app for chatting with Google's Gemini models.

These are self-contained single-page applications that run entirely in the browser, using API calls to the respective services. No server-side setup is required.

## Features

### Mini ChatGPT (1index.html)
- Supports multiple conversations with local storage persistence.
- Sidebar for managing and switching between chats.
- Model selection (e.g., GPT-4o-mini or GPT-4.1-mini).
- Requires an OpenAI API key.
- Messages are displayed in a dark-themed UI with user/assistant distinction.
- Enter key support for sending messages.
<img width="1918" height="872" alt="image" src="https://github.com/user-attachments/assets/f8f0af4d-bf0e-495d-9a52-747272526c18" />

### Gemini Chat (2index.html)
- Single conversation mode with a "New Chat" button to reset.
- Tracks total tokens used in the session.
- Light-themed UI with user/AI message bubbles.
- Requires a Google Generative Language API key.
- Direct API integration for Gemini-2.0-flash-001 (configurable).
<img width="1918" height="876" alt="image" src="https://github.com/user-attachments/assets/6c40fa26-ba7f-495f-a8d6-57cb77e9fbdd" />

## Requirements
- A modern web browser (e.g., Chrome, Firefox).
- An active API key:
  - For Mini ChatGPT: From [OpenAI](https://platform.openai.com/account/api-keys).
  - For Gemini Chat: From [Google AI Studio](https://aistudio.google.com/app/apikey) (for the Generative Language API).
- Internet access for API calls.

## Setup and Usage

1. **Download the Files**:
   - Save `1index.html` and `2index.html` to your local machine.

2. **Run the Apps**:
   - Open each file directly in your browser (e.g., double-click or use `file://` URL).
   - No installation or dependencies needed—the apps use vanilla JavaScript and fetch API.

3. **Mini ChatGPT Usage**:
   - Enter your OpenAI API key in the input field at the top of the sidebar.
   - Select a model from the dropdown.
   - Click "+ New Chat" to start a new conversation.
   - Type your message in the input field and click "Send" (or press Enter).
   - Conversations are saved in your browser's localStorage and listed in the sidebar.

4. **Gemini Chat Usage**:
   - The API key is hardcoded in the script (line ~28: `const API_KEY = "YOUR_KEY_HERE";`). Replace it with your actual key before use.
   - Type your message in the input field and click "Send".
   - Click "🆕 New Chat" to clear the conversation history.
   - Token usage is displayed at the top and updates after each response.

## Customization
- **API Keys**: Always keep your API keys secure. Do not share these HTML files with embedded keys.
- **Models**: You can modify the model names in the JavaScript code (e.g., change `MODEL` in Gemini Chat or add options in Mini ChatGPT).
- **Styling**: CSS is inline; edit the `<style>` blocks to customize the UI.
- **Error Handling**: Basic console logging is included; enhance as needed for production use.

## Limitations
- These are demo apps—API usage may incur costs based on your provider's pricing.
- No advanced features like image uploads, streaming responses, or error retries.
- Browser-based, so API keys are exposed in client-side code (use for personal testing only).
- Gemini Chat uses a fixed model; update the `MODEL` constant to experiment with others.

## Troubleshooting
- **API Errors**: Check the browser console for details (e.g., invalid key or rate limits).
- **CORS Issues**: APIs are called directly; ensure your keys have appropriate permissions.
- **LocalStorage**: Clear browser storage if conversations don't load properly.

## License
This project is open-source under the MIT License. Feel free to modify and redistribute.

For questions or contributions, open an issue or pull request if this is hosted on a repo.
