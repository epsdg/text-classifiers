## Pretrained Text Classifiers

Jupyter/Colab notebooks with implementations of several pretrained language models for classification.

### TensorFlow Models (TPU)
 - [XLNet](https://arxiv.org/abs/1906.08237)
 - [BERT](https://arxiv.org/abs/1810.04805)

Based on original Google AI Research (BERT) and CMU/Google Brain (XLNet) implementations. Tested in colab using a cloud TPU v2.  These support both binary and multi-label classification.

The models require I/O via Google Cloud Storage instead of the local file system attached to the colab instance.

### PyTorch Models (GPU)
 - [OpenAI GPT](https://openai.com/blog/language-unsupervised/)
 - [OpenAI GPT2](https://openai.com/blog/better-language-models/)
 - [BERT](https://arxiv.org/abs/1810.04805)

The PyTorch models currently support only binary classification.

Models were tested in colab using 1x NVIDIA Tesla T4 GPU.  They will run on other CUDA devices with less memory, but require constraints on maximum sequence length and/or batch size, with significant impact on train time.

The models use [NVIDIA Apex](https://github.com/NVIDIA/apex) for mixed-precision scaling during training.

BERT uses the [Hugging Face port](https://github.com/huggingface/pytorch-pretrained-BERT) of the original models to PyTorch

The OpenAI models (GPT & GPT2) use a [fork](https://github.com/epsdg/pytorch-pretrained-BERT) of the above repo with a modification to support binary classification.
