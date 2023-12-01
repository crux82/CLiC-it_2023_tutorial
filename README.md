### CLiC-it 2023 Tutorial

# Large Language Models and How to Instruction Tune Them (in a Sustainable Way)

### **Authors**: [Danilo Croce](https://scholar.google.it/citations?user=dXewdYAAAAAJ&hl=it) & [Claudiu Daniel Hromei](https://scholar.google.it/citations?user=YQRKKFoAAAAJ&hl=it)

This repository hosts materials from the [CLiC-IT 2023 tutorial](https://clic2023.ilc.cnr.it/tutorial/), aiming to:

The **objective of this tutorial** is:

* **Introduce Transformer-based architectures**, including encoding-decoding, encoder-only, and decoder-only structures.
* **Demonstrate fine-tuning of Large Language Models** (LLMs) on diverse datasets in a multi-task framework.
* Utilize [Low-Rank Adaptation](https://arxiv.org/abs/2106.09685) (LoRA) for **sustainable and efficient tuning** on "modest" hardware (e.g., single 16GB RAM GPU).

The repository includes code for fine-tuning a Large Language Model (based on [LLaMA](https://ai.meta.com/blog/large-language-model-llama-meta-ai/)) with instructions to solve all the tasks from [EVALITA 2023](https://www.evalita.it/campaigns/evalita-2023/). 
In particular, this tutorial shows how to encode data from different tasks into specific prompts and fine-tune the LLM using [Q-LoRA](https://arxiv.org/abs/2305.14314). The code can be also used in Google Colab using an Nvidia-T4 GPU with 15GB memory.

The code is heavily based on the one used in ExtremITA system participating to EVALITA 2023:

* [ExtremITA Paper](https://ceur-ws.org/Vol-3473/paper13.pdf)
* [ExtremITA Github Code](https://github.com/crux82/ExtremITA)

### Code

The overall process is divided in four steps:

* [**Step 1 - Encoding the data**](https://github.com/crux82/CLiC-it_2023_tutorial/blob/main/CLiC_it_2023_tutorial_ExtremITA_0_data_encoder.ipynb): it shows how to encode data from an EVALITA task to generate prompts for the LLM
* [**Step 2 - Fine-tuning the LLaMA model**](https://github.com/crux82/CLiC-it_2023_tutorial/blob/main/CLiC_it_2023_tutorial_ExtremITA_1_train.ipynb): it shows how to fine-tune the LLMS given the prompts 
* [**Step 3 - Inference: generating answers**](https://github.com/crux82/CLiC-it_2023_tutorial/blob/main/CLiC_it_2023_tutorial_ExtremITA_2_inference.ipynb): it shows how to use the fined-tuned model
* [**Step 4 - Deconding the data**](https://github.com/crux82/CLiC-it_2023_tutorial/blob/main/CLiC_it_2023_tutorial_ExtremITA_3_data_decoder.ipynb): it shows how to conver the data to be evaluated in the EVALTA challenge

### Slides

The repository also features **tutorial slides** ([LINK](https://github.com/crux82/CLiC-it_2023_tutorial/blob/main/CLIC2023_tutorial.pdf)).

For queries or suggestions, raise an Issue in this repository or email  [croce@info.uniroma2.it](mailto:croce@info.uniroma2.it) or [hromei@ing.uniroma2.it](mailto:hromei@ing.uniroma2.it).


