# 🌍 City Fact Extractor

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)  
![License](https://img.shields.io/badge/license-MIT-blue)  
![Version](https://img.shields.io/badge/version-1.0.0-blueviolet)

---

## 🧠 Description

**City Fact Extractor** is an AI-powered application that transforms plain Wikipedia city summaries into quirky, culturally interesting facts. Whether you're a trivia enthusiast, app developer, or travel lover, this tool adds flair and fun to your city data.

Choose from different styles like **funny**, **poetic**, or **formal**, and even personalize the output with your name!

---

## ✨ Features

- 🎯 Extracts **exactly 3 quirky or culturally interesting facts** per city.
- 🌐 Supports **multiple cities** in one query.
- 🎭 Outputs in various styles: *funny*, *poetic*, or *formal*.
- 💡 Appends a **"Did you know?"** fact per city.
- 🙋 Personalized greetings when a **user name** is provided.
- 🧩 Built on an **AI agent-based** architecture using inline YAML-style configuration logic.

---

## 🚀 Installation

### 🔧 Prerequisites

- Python 3.8+
- [Docker](https://www.docker.com/get-started) *(optional for containerized deployment)*
- EC2 or local machine (Ubuntu/Windows/Linux)

---

## 📦 Setup Instructions

1. **Clone the Repository**
   
   git clone https://github.com/yourusername/city-fact-extractor.git
   cd city-fact-extractor
Create and Activate a Virtual Environment (optional but recommended)


python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
Install Dependencies
(Add any specific libraries your project uses)

pip install -r requirements.txt
Set Environment Variables (optional, see below)

Run the Script


python run_extract_facts.py --input inputs.yaml


⚙️ Usage

inputs = {
    "cities": ["Paris", "Tokyo"],
    "summaries": {
        "Paris": "Paris is the capital of France, known for the Eiffel Tower, cafes, and rich culture.",
        "Tokyo": "Tokyo is the capital of Japan, famous for its skyscrapers, technology, and cherry blossoms."
    },
    "style": "funny",  # Options: "funny", "poetic", "formal"
    "username": "Ansh"  # Optional
}

{
  "Paris": {
    "greeting": "Hey Ansh! Ready for some quirky Paris facts?",
    "facts": [
      "Paris once had a law allowing men to pee in the streets — classically French!",
      "The Eiffel Tower grows in summer – about 6 inches due to heat!",
      "French bread has legal requirements — even in how it's baked!",
      "Did you know? There's only one stop sign in all of Paris!"
    ]
  },
  "Tokyo": {
    "greeting": "Hey Ansh! Here’s what’s buzzing in Tokyo!",
    "facts": [
      "Tokyo has vending machines for everything — including eggs and umbrellas!",
      "It's illegal to dance past midnight — well, it was until 2015!",
      "Shibuya Crossing sees more foot traffic than Times Square!",
      "Did you know? Tokyo has more Michelin stars than any city in the world!"
    ]
  }
}
🧩 Internal Configuration (No YAML Files Needed)
The logic mimics agent/task architecture using inline configurations like:


agent_config = {
    "goal": "Extract quirky, engaging facts about a city from its summary.",
    "style_options": ["funny", "poetic", "formal"],
    "tasks": [
        "Extract 3 unique facts from the summary",
        "Add 1 extra 'Did you know?' style fact",
        "Format output in the chosen style"
    ]
}
🔐 Environment Variables (Optional)
If you're using external APIs like OpenRouter or deploying via AWS, set these:

Variable	Description	Example
OPENROUTER_API_KEY	API key for OpenRouter AI model	abcdef123456
AWS_ACCESS_KEY_ID	AWS credentials for EC2 access	AKIAIOSFODNN7EXAMPLE
AWS_SECRET_ACCESS_KEY	AWS secret access key	wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY

Set them in .env or directly in your terminal.

🧪 Sample Output (Funny Style)
text
Copy code
City: Paris

Hey Ansh! Ready for some quirky Paris facts?

1. Paris once had a law allowing men to pee in the streets — classically French!
2. The Eiffel Tower grows in summer – about 6 inches due to heat!
3. French bread has legal requirements — even in how it's baked!
Did you know? There's only one stop sign in all of Paris!
🧰 Technologies Used
Python for logic and processing

OpenRouter / Meta LLaMA for language model API

Wikipedia as the data source

Docker (optional) for containerization

Amazon EC2 for deployment (optional)

Inline configuration (no external YAML files required)

📸 Screenshots / Demo
(You can add screenshots or screen recordings here once available)

🧪 Running Tests
If you have test scripts, run:


pytest tests/
Or use your own test runner.

🤝 Contributing
We welcome contributions!

Fork the repository

Create a new branch:


git checkout -b feature-name

Make changes and commit:
git commit -m "Added new feature"
Push and create a Pull Request:


git push origin feature-name
Please follow the project’s style and include tests if applicable.

📜 License
This project is licensed under the MIT License. See the LICENSE file for more information.

❓ FAQ
Q: Can I add more output styles like sarcastic or romantic?
A: Yes, just add the style option in the input and modify the logic to reflect tone.

Q: How do I add more cities?
A: Extend the cities list and add corresponding summaries in the summaries dictionary.

Q: Is this scalable for many cities at once?
A: Yes, but be mindful of API rate limits and consider batching requests for best performance.

📬 Contact
Ansh Tiwari
📧 Email: tiwariansh1308@gmail.com
💻 GitHub: AnshT013
🔗 LinkedIn: Ansh Tiwari

🙏 Acknowledgements
🧠 Wikipedia for open access to city data

🤖 OpenRouter for natural language generation

🔧 Inspired by Julep Agent-based workflow

🙌 Thanks to the open-source community!