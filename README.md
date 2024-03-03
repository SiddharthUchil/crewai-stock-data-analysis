# Financial Statement Analysis with CrewAI

This project uses the [CrewAI] framework to analyze financial statements for any company or stock using the [QuickFS] API and [matplotlib]. The project consists of two main components:

- A data loader agent that fetches financial data from the QuickFS API based on the user's input of a company name, a stock symbol, and a metric of interest. The data loader agent uses the [langchain_community] package to access the QuickFS API and the [langchain_openai] package to use the OpenAIGPT4 model as the LLM.
- A chart generator agent that creates a bar chart of the financial metric over time using matplotlib and saves it as an image file. The chart generator agent also uses the OpenAIGPT4 model as the LLM.

The project outputs a markdown file that contains the chart image of the financial metric trend. The markdown file can be uploaded to a GitHub repository as a README.md file.

## Installation and Usage

To run this project, you need to install the following packages:

```bash
pip install crewai
pip install langchain_community
pip install langchain_openai

```
You also need to obtain an API key from QuickFS and set it as an environment variable:
export QUICKFS_API_KEY=your_api_key

To run the project, you can use the following command:

```bash
python main.py

```

The project will prompt you to enter a company name or a stock symbol, and a financial metric. 
For example, you can enter AAPL for Apple Inc. and revenue for the revenue metric. 
The project will then fetch the data from the QuickFS API and generate a chart using matplotlib. 
The project will also create a markdown file report.md that contains the chart image of 
the metric trend. You can view the markdown file in any markdown viewer or upload it to your GitHub repository 
as a README.md file.