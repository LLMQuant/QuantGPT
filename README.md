
# QuantGPT

**QuantGPT** leverages the power of Large Language Models (LLMs) to enhance Retrieval-Augmented Generation (RAG) in finance. By providing more accurate and contextually relevant information, QuantGPT efficiently retrieves and synthesizes financial data from diverse sources to generate insightful analyses, forecasts, and recommendations.

## Table of Contents
- [QuantGPT Overview](#quantgpt-overview)
- [Components](#components)
  - [Data Retrieval](#data-retrieval)
  - [Data Synthesis](#data-synthesis)
  - [Analysis and Forecasting](#analysis-and-forecasting)
  - [Recommendations](#recommendations)
- [Installation](#installation)
- [Usage](#usage)
  - [Data Retrieval](#data-retrieval-usage)
  - [Data Synthesis](#data-synthesis-usage)
  - [Analysis and Forecasting](#analysis-and-forecasting-usage)
  - [Recommendations](#recommendations-usage)
- [File Structure](#file-structure)
- [License](#license)

## QuantGPT Overview

QuantGPT is designed to utilize LLMs to improve the accuracy and contextual relevance of financial information retrieval and generation. In RAG systems, QuantGPT retrieves and synthesizes financial data from various sources, including market reports, financial news, and historical data, to generate comprehensive analyses, forecasts, and actionable recommendations.

## Components

### Data Retrieval

QuantGPT efficiently retrieves relevant financial data from multiple sources, ensuring that the information is accurate and up-to-date.

### Data Synthesis

Using advanced language understanding, QuantGPT synthesizes the retrieved data to create coherent and contextually relevant summaries and reports.

### Analysis and Forecasting

QuantGPT leverages the synthesized data to perform in-depth analyses and generate forecasts, providing valuable insights into market trends and financial performance.

### Recommendations

Based on the analyses and forecasts, QuantGPT generates actionable recommendations for investment strategies and financial planning.

## Installation

**1. (Recommended) Create a new virtual environment**
```shell
conda create --name quantgpt python=3.10
conda activate quantgpt
```

**2. Download the QuantGPT repository**
```shell
git clone https://github.com/YourUsername/QuantGPT.git
cd QuantGPT
```

**3. Install QuantGPT & dependencies from source or PyPI**
```bash
pip install -U quantgpt
```
or
```bash
pip install -e .
```

**4. Configure API keys**
```shell
1. Rename `OAI_CONFIG_LIST_sample` to `OAI_CONFIG_LIST` and add your OpenAI API key.
2. Rename `config_api_keys_sample` to `config_api_keys` and add your financial data API keys.
```

## Usage

### Data Retrieval Usage
To retrieve financial data:
```python
from quantgpt.data_retrieval import DataRetriever

retriever = DataRetriever(config)
data = retriever.retrieve()
```

### Data Synthesis Usage
To synthesize retrieved data:
```python
from quantgpt.data_synthesis import DataSynthesizer

synthesizer = DataSynthesizer(config)
summary = synthesizer.synthesize(data)
```

### Analysis and Forecasting Usage
To perform analysis and generate forecasts:
```python
from quantgpt.analysis import Analyzer

analyzer = Analyzer(config)
forecast = analyzer.forecast(data)
```

### Recommendations Usage
To generate investment recommendations:
```python
from quantgpt.recommendations import Recommender

recommender = Recommender(config)
recommendations = recommender.recommend(forecast)
```

## File Structure

The main folder **quantgpt** has three subfolders **data_retrieval, data_synthesis, analysis**. 

```
QuantGPT
├── quantgpt (main folder)
│   ├── data_retrieval
│   	├── data_retriever.py
│   ├── data_synthesis
│   	├── data_synthesizer.py
│   ├── analysis
│   	├── analyzer.py
│   ├── recommendations
│   	├── recommender.py
│   ├── utils.py
│
├── configs
├── experiments
├── tutorials (hands-on tutorial)
│   ├── data_retrieval_tutorial.ipynb
│   ├── data_synthesis_tutorial.ipynb 
│   └── analysis_tutorial.ipynb
├── setup.py
├── config_api_keys_sample
├── requirements.txt
└── README.md
```

## License

This project is licensed under the Apache-2.0 License. See the LICENSE file for more details.

---

**Disclaimer**: The information provided in this repository is for educational purposes only and should not be construed as financial advice. Always consult with a qualified financial advisor before making any investment decisions.
