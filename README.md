# Fashion-Analyzer-with-Computer-Vision-and-RAG
[![Python 3.11+](https://img.shields.io/badge/Python-3.11%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.5.1-red?logo=pytorch&logoColor=white)](https://pytorch.org/)
[![IBM Watson AI](https://img.shields.io/badge/IBM%20Watson-AI-0F62FE?logo=ibm&logoColor=white)](https://www.ibm.com/cloud/watson)
[![Gradio](https://img.shields.io/badge/Gradio-5.22.0-orange?logo=gradio&logoColor=white)](https://www.gradio.app/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.5.2-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-green)](LICENSE)

A multimodal AI application that analyzes fashion images and provides detailed style recommendations using computer vision and large language models.

## Features

- **Image Analysis**: Upload fashion images and get detailed style breakdowns
- **Similarity Matching**: Find visually similar items from a curated dataset
- **AI-Powered Descriptions**: Llama Vision model generates professional fashion analysis
- **Price Alternatives**: Discover similar items across different price points
- **Web Interface**: User-friendly Gradio application for easy interaction

## Technology Stack

| Component | Technology |
|-----------|------------|
| **Image Encoding** | ResNet50 (TorchVision) |
| **Similarity Search** | Scikit-learn Cosine Similarity |
| **Vision-Language Model** | Meta Llama 4 Vision Instruct |
| **ML/AI Platform** | IBM Watson AI |
| **Web Interface** | Gradio |
| **Deep Learning** | PyTorch |

## Quick Start

### Prerequisites
- Python 3.11+
- Virtual environment

### Installation

'''bash
# Clone repository
git clone <repo-url>
cd style-finder

# Create virtual environment
python3.11 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt


## How It Works
1. *Upload Image*: User provides a fashion photo
2. *Encode Image*: ResNet50
converts image to feature vector
3. *Find Match*: Similarity search identifies visually similar items
4. *Retrieve Data*: System gathers all related products
5. *Generate Analysis*: Llama model creates detailed fashion description
6. *Display Results*: Professional recommendations with product links and prices

## Architecture
   User Image
   │
   ▼
┌──────────────────┐
│  ImageProcessor  │  (ResNet50 → base64 + feature vector)
└──────────────────┘
   │
   ▼
┌──────────────────┐
│  Vector Search   │  (cosine similarity vs dataset embeddings)
└──────────────────┘
   │
   ▼
┌──────────────────┐
│  LlamaVision     │  (image + retrieved context → analysis)
│  Service         │
└──────────────────┘
   │
   ▼
┌──────────────────┐
│  Gradio UI       │  (upload, examples, markdown output)
└──────────────────┘
## Dataset
Fashion items sourced from Taylor Swift's iconic outfits, including item names, prices, and purchase links.
## License
Apache 2.0

*Built with IBM Watson Al | Powered by Meta Llama Vision*
