# Lingvanex Interview Task
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Test task for the position of Junior Python Developer at [Lingvanex](https://lingvanex.com/)[WikiMatrix.en-ru.en](dataset%2FWikiMatrix.en-ru.en)

## Description
Filter the dataset as best you can using [Opus filters](https://github.com/Helsinki-NLP/OpusFilter). The dataset consists of 2 text files ([WikiMatrix.en-ru.en](dataset/WikiMatrix.en-ru.en) and [WikiMatrix.en-ru.ru](dataset/WikiMatrix.en-ru.ru) ) and contains translations of sentences from English into Russian.

Your task is to remove lines where the translation from English into Russian is incorrect, where there are errors (grammatical, lexical, etc.).

## Getting Started

### Installing
1. Clone the repository:
```
git clone <repo>
```
2. Create and activate virtual environment:
```
virtualenv venv
source venv/bin/activate
```
3. Install the required dependencies:
```
pip install -r requirements.txt
```
4. Set up your `config.yaml` file. For more details see [Basic usage](https://helsinki-nlp.github.io/OpusFilter/usage.html)

### Executing program
Run the following command to execute all steps from your configuration:
```
opusfilter config.yaml
```
or run a single-step configuration using just command line arguments:
```
opusfilter-cmd filter --inputs dataset/WikiMatrix.en-ru.en dataset/WikiMatrix.en-ru.ru --outputs dataset/WikiMatrix_filtered.en dataset/WikiMatrix_filtered.ru --filters '[{"LengthFilter": {"unit": "word", "min_length": 1, "max_length": 100}}]'
```

## What can be improved
- [ ] Cover the code with tests
- [ ] Add custom filter
- [ ] Add custom preprocessor