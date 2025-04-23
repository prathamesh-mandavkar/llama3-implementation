# LLaMA 3 Implementation

A PyTorch implementation of Meta's LLaMA 3 architecture. This repository contains code for training and evaluating a smaller version of the LLaMA 3 language model.

## Overview

This project implements the LLaMA 3 architecture from scratch using PyTorch. It includes:

- Tokenizer implementations trained on the Tiny Shakespeare dataset
- Model training code and pre-trained weights
- Inference and evaluation utilities

The implementation is based on insights from the LLaMA 3 research paper and inspired by similar efforts to reproduce transformer-based language models.

## Repository Structure

```
llama3-implementation/
│
├── models/                        # Trained model checkpoints
│   ├── Llama3_2024-10-05_23-12-27.json  # Model configuration
│   └── Llama3_2024-10-05_23-12-27.pth   # Model weights
│
├── tokenizers/                    # Tokenizer models with different vocabulary sizes
│   ├── tiny_shakespeare_tokenizer_128.model
│   ├── tiny_shakespeare_tokenizer_256.model
│   ├── tiny_shakespeare_tokenizer_512.model
│   └── tiny_shakespeare_tokenizer_1024.model
│
├── tiny_shakespeare_tokenizer.py  # Tokenizer implementation
├── input.txt                      # Sample input text
└── llama3_implementation.ipynb    # Training and evaluation notebook
```

## Getting Started

### Prerequisites

- Python 3.8+
- PyTorch 2.0+
- Jupyter Notebook (for running the included notebook)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/prathamesh-mandavkar/llama3-implementation.git
cd llama3-implementation
```

2. Install the required dependencies:
```bash
pip install torch numpy tqdm matplotlib jupyter
```

### Usage

#### Training a Model

Execute the training code in `llama3_implementation.ipynb` or use the provided pre-trained models in the `models/` directory.

## Training Details

The model was trained on the Tiny Shakespeare dataset, following architectural principles from the LLaMA 3 paper. The implementation includes attention mechanisms, positional encodings, and feed-forward networks characteristic of modern transformer-based language models.

## References

This implementation draws inspiration from:

- [LLaMA 3 Research Paper](https://ai.meta.com/research/publications/llama-3-a-more-capable-open-language-model-family/)
- [Andrej Karpathy's "Let's reproduce GPT-2 (124M)"](https://youtu.be/l8pRSuU81PU?si=5FuXWc6VJghGZBr0)
- [Let's build the GPT Tokenizer](https://youtu.be/zduSFxRajkE?si=FtokVhpIZZPZSzOR)
- [Tunadorable](https://youtu.be/lZj8F6EspVU?si=RtVR4sJ6PbHdC5W6)

## License

This project is available under the MIT License - see the LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
