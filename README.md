# Email ADK Agent

An ADK-based agent that composes and sends emails on your behalf via Gmail.

## Setup

1. Create a virtual environment and install dependencies:

   ```bash
   python -m venv venv
   venv\Scripts\activate      # Windows
   pip install -r requirements.txt
   ```

2. Create a `.env` file in the project root with your API keys:

   ```
   GEMINI_API_KEY=your_key_here
   PINECONE_API_KEY=your_key_here
   GROQ_API_KEY=your_key_here
   ```

3. Download an OAuth 2.0 "Desktop app" client from the Google Cloud Console
   (Gmail API enabled) and save it as `credentials.json` in the project root.

   On first run, a browser window will open for consent, and a `token.json`
   will be cached automatically.

   **Note:** `.env`, `credentials.json`, and `token.json` are gitignored and
   must never be committed — they contain secrets specific to your account.

## Usage

Run the agent with the ADK CLI/dev UI from the project root, e.g.:

```bash
adk run email_agent
```
