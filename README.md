# Qualitative Data Analysis 📝

This tool helps you perform qualitative data analysis by generating codes and themes from your transcripts, summarizing your data, and providing insights. 📊

## 🔬 Tech Stack

The Qualitative Data Analysis uses [LLMs](https://en.wikipedia.org/wiki/Large_language_model) (Large Language Models) to generate summaries, codes, themes, and classify them. The application is developed with Python.

### Python Libraries

This tool is powered by the following libraries:

- [Streamlit](https://streamlit.io): For the User Interface 🖥️
- [Langchain](https://langchain.com): For creating LLMs applications 🔗
- [OpenAI](https://openai.com): The LLMs provider. Currently, only this LLM is integrated.

## Getting Started 🏁

### Requirements

Ensure you have [Python](https://www.python.org/downloads/) installed on your computer. Use the latest version of Python 3. The tested version is 3.8.10. 🐍

### Configuration

Rename the `.streamlit/secrets_template.toml` file to `.streamlit/secrets.toml` and edit it to add your own configuration for Langchain, Langsmith, and OpenAI API key.

### Installation

Clone the repository and install the dependencies:

```bash
git clone
cd qualitative-data-analysis
pip install -r requirements.txt
```

### Run the Application

```bash
streamlit run source/qualitative_analyse_agent.py
```

## Usage 📖

1. **Upload your transcripts:** Upload your transcripts from the sidebar. 📂
   - **Generate transcripts summary:** In the Raw data section, you can generate a summary of your data individually.
2. **Enter your research question:** Input your research question, which will be used to generate codes and themes. ❓
3. **Generate codes and themes:** Click the button to generate codes and themes based on your research question. 💡

## Langsmith Integration 🔗

Use Langsmith to monitor your application and get insights on its usage. 📊

Edit the `.streamlit/secrets.toml` file and add the following lines:

```toml
[langsmith]
tracing = true
api_url = "https://api.smith.langchain.com"
api_key = "your key here"
project = "your project here"
```

## Diagrams

### Libs

TODO: Show a diagram with the interaction between libraries.

### LLM Chain

TODO: Show the LLM Chaining.

## Features ✨

- Upload your transcripts 📂
- Generate summary on all data or specific data 📊
- Generate codes and themes based on a research question ❓
- Update Qualitative Analysis Data parameters 🔄
- Generate and download a Qualitative Data Analysis report 📄

## Limitations ⚠️

- The tool cannot perform Qualitative Data Analysis on large datasets as the LLM used is limited to 16000 tokens. 🚫
- The data and report are not cached. If you reset the page, the data will need to be re-uploaded, and the report regenerated. 🔄

## Improvements 🚀

- Upload voice transcripts, convert them to text, and perform Qualitative Data Analysis 🗣️
- Connect to Qualitative Data software 🤝
- Perform intermediate checks on results to avoid LLM bias 🤔
- Perform map-refine summary on the data
- Handle large data transcripts

Made with ❤️
