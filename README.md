#  Cybersecurity Incident Response Assistant

An AI-powered assistant that helps users quickly and effectively respond to cybersecurity incidents like phishing attacks, credential leaks, and device loss. Built using Google FLAN-T5, Gradio, and a simple intent-entity matching system, this tool provides step-by-step action protocols based on the type of incident described.

---

##  Features

-  Detects incident intent (e.g., phishing, credential leak) from user input.
-  Uses FLAN-T5 to generate context-aware response plans.
-  Templates for multiple cybersecurity incidents.
-  Easily extensible with more incidents and response types.
-  User-friendly interface via [Gradio](https://gradio.app).

---

## Project Structure

├── incidents.json # Knowledge base of incident types and examples
├── app.ipynb      # Main Colab notebook with UI and logic
├── README.md      # You’re here

---

## 🛠 How It Works

1. **Input**: User describes an incident (e.g., "I entered my password on a fake login page").
2. **Intent Detection**: The system detects the type of incident (e.g., `phishing`, `credential_leak`) using keyword-based matching (can be replaced with NLP model).
3. **Prompt Generation**: A prompt template is filled using incident-specific entities.
4. **AI Response**: Google FLAN-T5 generates a detailed incident response protocol.
5. **Output**: The response is shown in a clean Gradio interface.

---

##  Try It Out

If running locally (optional), install the dependencies:

```bash
pip install transformers sentence-transformers gradio pandas
Then run the app: "python app.py"
If using Google Colab, just open the notebook and run all cells.
