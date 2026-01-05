## Congen.ai – Automated Course Content Generator 🤖

Congen.ai is an AI‑powered course content generator that helps educators, instructional designers, and creators go from a simple topic to a complete curriculum with quizzes and exportable teaching materials that uses Perplexity’s LLM API to turn a topic and audience profile into structured modules, lessons, and quizzes, with export to PDF and PPT for instant teaching‑ready materials.

## 📘 Introduction

Congen.ai is a personal project built to reduce the time and friction involved in planning and drafting courses. It takes high‑level inputs such as course name, target audience education level, difficulty, duration, and credits, then generates a structured course outline with modules, lessons, and assessments.

The system also supports quiz generation and exports the full course package as PDF and PPT, making it easy to plug into existing training, LMS, or slide‑based workflows.

## 🤖 How Congen.ai Uses Perplexity LLM

Congen.ai uses Perplexity’s LLM API as the main language model backend, leveraging fast inference and access to strong open‑source models such as Llama and Mistral families through pplx‑api.  The app calls Perplexity’s chat endpoints to generate outlines, expand lessons, and draft quizzes based on the user’s course parameters.

Perplexity’s optimized inference layer (built on NVIDIA TensorRT‑LLM with A100 GPUs) keeps generation responsive while allowing experimentation with different model variants exposed via pplx‑api.[2]

## 🌟 Features

- **Interactive customization**: Enter course topic, target audience level, difficulty, number of modules, duration, and credits to generate a tailored course outline.  
- **Detailed content generation**: Expand each module into lesson‑level content with learning objectives, key concepts, and suggested activities.  
- **Quiz generation**: Automatically create quizzes for each module, aligned to the generated content and difficulty level.  
- **PDF export**: Download the complete course as a well‑formatted PDF for offline use or sharing.  
- **PPT export**: Export the course into a PowerPoint deck, ready for delivery or further editing.  

## 🧱 Tech Stack & Structure

- **Tech stack**:  
  - Python for core logic and orchestration.  
  - Streamlit for the interactive web UI.  
  - Perplexity LLM API (pplx‑api) as the primary language model provider, with access to optimized Llama/Mistral‑class models.
  - Prompt modules for outline, detailed content, and quiz generation.

- **Project structure**:

  ```text
  congen-ai/
  │
  ├── prompts/
  │   ├── tabler_prompt.py      # outline and table-style structures
  │   ├── dictator_prompt.py    # detailed lesson/module content
  │   └── quizzy_prompt.py      # quiz and assessment generation
  │
  ├── app.py                    # main Streamlit application
  ├── README.md
  ├── requirements.txt
  └── .env.example              # Perplexity API key and model configuration
  ```

The `.env.example` file documents how to set the Perplexity API key and select the default model used for generation via pplx‑api.

## 💼 My Role, Impact & Outcomes

- **Key contributions**:  
  - Designed and implemented the Streamlit front‑end, including the multi‑step flow from “idea → outline → full content → exports”.  
  - Implemented prompt‑engineering patterns for separate phases (outline, detailed content, quizzes) to keep generations controllable and easy to iterate on.  
  - Integrated Perplexity’s LLM API, plus PDF and PPT export, to create an end‑to‑end course creation pipeline.

- **Impact**:  
  - Demonstrated a 70–80% reduction in course development time for test curricula by automating outline and first‑draft content creation.  
  - Enabled educators to tailor courses to specific audience levels and difficulties while keeping structure and learning goals consistent.  

## 🚀 Usage

1. Clone the repository and create a Python virtual environment.  
2. Install dependencies from `requirements.txt`.  
3. Create a `.env` file based on `.env.example` and set your Perplexity API key and model name.
4. Run the app with:

   ```bash
   streamlit run app.py
   ```

5. Open the local URL in your browser, enter course details, generate the outline and full content, then export to PDF or PPT as needed.

## ⚖️ License

This project is licensed under the MIT License. See the `LICENSE` file for details.


