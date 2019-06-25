## Pretrained Text Classifiers

Jupyter/Colab notebooks with imlementations of [BERT](https://arxiv.org/abs/1810.04805) and OpenAI [GPT](https://openai.com/blog/language-unsupervised/) and [GPT2](https://openai.com/blog/better-language-models/) for binary classification.

Models were tested in Colab using 1x NVIDIA Tesla T4 GPU.  They will run on other CUDA devices with less memory, but require constraints on maximum sequence length and/or batch size, with significant impact on train time.

The models use [NVIDIA Apex](https://github.com/NVIDIA/apex) for mixed-precision scaling during training.

BERT uses the [Hugging Face port](https://github.com/huggingface/pytorch-pretrained-BERT) of the original models to PyTorch

The OpenAI models (GPT & GPT2) use a [fork](https://github.com/epsdg/pytorch-pretrained-BERT) of the above repo with a modification to support binary classification.
