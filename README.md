# OpenaiFineTuneExample

This repository showcases how to fine-tune OpenAI models using custom datasets in JSONL format.

## Overview

Fine-tuning a model allows users to adapt a pretrained model to better suit specific domains or use cases. This example demonstrates the process for preparing a custom dataset, uploading it, and using the fine-tuned model for generating responses.

## Prerequisites

- An active OpenAI account and API key.
- Python 3.9 or later.
- Required Python libraries: `openai`

## Setup

1. Clone this repository:

```bash
git clone https://github.com/Haku247/OpenaiFineTuneExample.git
cd OpenaiFineTuneExample
```

2. Install the required Python packages:

```bash
pip install -r requirements.txt
```

3. Set up your OpenAI API key:

You can set your API key in the `.env` file:

```
OPENAI_API_KEY=your_openai_api_key_here
```

## Usage

### Using the provided `school_library_qa.json` example:

1. Generate the training dataset in JSONL format:

```bash
python finetune.py generate_training_dataset school_library_qa.json "You are an intelligent assistant in a school library."
```

2. Upload the training dataset:

```bash
python finetune.py upload_training_dataset training_dataset.jsonl
```

3. Use the fine-tuned model:

```bash
python finetune.py ask your_model_name "You are an intelligent assistant in a school library." "Do you have books on history?"
```

### For custom datasets:

1. Generate the training dataset in JSONL format:

```bash
python finetune.py generate_training_dataset input.json "Your system message here"
```

2. Upload the training dataset:

```bash
python finetune.py upload_training_dataset training_dataset.jsonl
```

3. Use the fine-tuned model:

```bash
python finetune.py ask your_model_name "Your system message here" "Your user input here"
```

## License

This project is licensed under the MIT License.
