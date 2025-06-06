# 🌍 Extract City Facts App

## Overview

**Extract City Facts App** is an AI-powered workflow that takes Wikipedia summaries of cities and produces **witty, poetic, or formal** fun facts. Powered by prompt engineering and YAML-based agent orchestration, this app demonstrates how to use AI for creative data extraction and personalized content generation.

This project uses a modular structure of AI agents and input-output workflows. It's perfect for exploring LLM orchestration, persona-based generation, and creative use of AI.

---

## 🎯 Purpose

This app was created to:

- Practice **prompt engineering**, **persona design**, and **context-aware generation**
- Extract **fun, quirky, or surprising facts** about cities
- Showcase how **multi-step AI agents** can work together in a pipeline
- Enable **custom output styles** like funny, poetic, or formal

---

## 🚀 Key Features

- ✅ **Multi-City Support**: Processes multiple cities and summaries in one go  
- 🧠 **Witty AI Agent**: Extracts facts with personality (poetic, funny, or formal tone)  
- 🛠️ **Composable YAML Agents**: Cleanly defined inputs, steps, and outputs  
- 🔄 **Loop-Based Processing**: Uses `foreach` to iterate over cities dynamically  
- 🎁 **Bonus Fact**: Each city includes a unique "Did you know?" surprise!  

---

## 🧑‍💻 How It Works

1. **Input**: A list of cities and their Wikipedia summaries  
2. **Agent Loop**: For each city, an AI agent (`city-fact-agent`) is called  
3. **Fact Generation**: The agent extracts 3 quirky facts + 1 bonus "Did you know?" fact  
4. **Output**: Returns a map of city → list of fun facts

---

## 🧱 Technologies Used

- 🧾 **YAML**: For defining structured agents and workflows  
- 🤖 **Meta LLaMA 4 - Maverick (Free)**: Model used via OpenRouter  
- ⚙️ **Prompt Engineering**: Custom instructions and multi-style output  
- 🪄 **Persona Design**: Witty assistant that adapts to user inputs  
- ☁️ **EC2 Ubuntu**: Deployment-ready on cloud (instructions included)

---

## ⚙️ Inputs & Customization

- **cities**: List of city names  
- **summaries**: Map of city → Wikipedia summary  
- **style** (optional): `poetic`, `funny`, or `formal`  
- **user_name** (optional): Personalized greeting support  

---

## 🌐 Live Demo (Coming Soon!)

Stay tuned for the live demo or host it using your preferred YAML orchestration engine. You can simulate inputs using Julep, LangChain, or local agents.

---

## 📸 Example Output

### **Paris**
- The Eiffel Tower was originally painted red.
- Paris has a vineyard in Montmartre.
- It’s illegal to name a pig ‘Napoleon’ in France.  
**Did you know?** Paris has more dogs than children!

---

### **Tokyo**
- Tokyo has cafes where you can cuddle hedgehogs.
- It has more Michelin-starred restaurants than any city in the world.
- There are vending machines that sell fresh eggs.  
**Did you know?** Tokyo has a museum entirely dedicated to parasites!

  ## 📁 Project Structure

![image](https://github.com/user-attachments/assets/2c42d816-afc1-45f2-b2bc-48fdcf8d5f3d)

## 🖥️ Deployment Guide (EC2)

Follow these steps to deploy the project on an **Ubuntu EC2 instance** (e.g., `t2.micro`):

### 1️⃣ Launch EC2 Instance

- Go to AWS EC2 Console.
- Launch a `t2.micro` instance with the **Ubuntu** AMI.

### 2️⃣ Connect via SSH

- Open your terminal and connect to the instance:.
- ssh -i your-key.pem ubuntu@your-ec2-ip.

### 3️⃣ Install Required Dependencies

- Update your package list and install Python, pip, and any other necessary tools:
- sudo apt update
- sudo apt install python3 python3-pip


## ✨ Customization Options

- **Personalized Greeting:** Add the `user_name` input to receive a warm, customized welcome.
- **Tone Styling:** Change the `style` input to:
  - `funny` – for a humorous tone
  - `poetic` – for an artistic tone
  - `formal` – for a polished, professional tone
- **Extendability:** You can create and plug in new agent types for different domains such as:
  - Food-related fun facts
  - Historical trivia
  - Cultural insights
## 👤 Author

**Ansh Tiwari**  
📧 Email: [tiwariansh1308@@gmail.com](mailto:tiwariansh1308@gmail.com)  
🔗 LinkedIn: [linkedin.com/in/ansh-tiwari-577a72246](https://www.linkedin.com/in/ansh-tiwari-577a72246/)  
💻 GitHub: [github.com/AnshT013](https://github.com/AnshT013)



