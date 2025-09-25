# 🤖 Ollama + DeepSeek Chatbot

A powerful Streamlit-based chatbot application that integrates both local Ollama models and cloud-based DeepSeek API, featuring OCR capabilities for image text extraction.

## ✨ Features

- **Multiple AI Models**: Support for various Ollama models and DeepSeek API
- **OCR Integration**: Extract text from uploaded images using EasyOCR
- **Chat Management**: Save, search, and manage conversation history
- **Real-time Communication**: Interactive chat interface with typing indicators
- **Model Selection**: Switch between different AI models on the fly
- **File Upload**: Support for JPG, JPEG, and PNG image formats

## 🚀 Supported Models

### Local Ollama Models
- Llama 3.2 1B (Fast)
- Llama 3.1 8B (Better)
- DeepSeek Coder 1.3B (Lightweight)
- DeepSeek Coder 6.7B (Powerful)

### Cloud API
- DeepSeek API (Cloud-based)

## 🛠️ Installation

### Prerequisites

1. **Python 3.8+**
2. **Ollama** installed and running locally
3. **DeepSeek API Key** (optional, for cloud features)

### Setup Steps

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/ollama-deepseek-chatbot.git
cd ollama-deepseek-chatbot
```

2. **Install dependencies**
```bash
pip install streamlit ollama openai easyocr
```

3. **Set up environment variables** (optional)
```bash
export DEEPSEEK_API_KEY="your_deepseek_api_key_here"
```

4. **Install and start Ollama**
```bash
# Install Ollama from https://ollama.ai
# Pull required models
ollama pull llama3.2:1b
ollama pull llama3.1:8b
ollama pull deepseek-coder:1.3b
ollama pull deepseek-coder:6.7b
```

## 🎯 Usage

1. **Start the application**
```bash
streamlit run app.py
```
2. **Access the web interface**
   - Open your browser and navigate to `http://localhost:8501`

3. **Select your preferred model**
   - Use the sidebar to choose between available models

4. **Start chatting**
   - Type your message in the text input
   - Upload images for OCR text extraction
   - Browse and search through chat history

## 📁 Project Structure
```
ollama-deepseek-chatbot/
│
├── app.py                 # Main Streamlit application
├── easyocr_helper.py      # OCR functionality helper
├── temp_uploads/          # Temporary directory for uploaded files
├── README.md             # Project documentation
└── requirements.txt      # Python dependencies
```

## 🔧 Configuration

### Environment Variables

- `DEEPSEEK_API_KEY`: Your DeepSeek API key for cloud-based inference

### Model Configuration

The application supports easy model switching through the sidebar. Models are configured in the `model_options` dictionary:

```python
model_options = {
    "Llama 3.2 1B (Fast)": "llama3.2:1b",
    "Llama 3.1 8B (Better)": "llama3.1:8b",
    "DeepSeek Coder 1.3B (Lightweight)": "deepseek-coder:1.3b",
    "DeepSeek Coder 6.7B (Powerful)": "deepseek-coder:6.7b",
    "DeepSeek API (Cloud)": "deepseek-api",
}
```

## 📸 OCR Features

- **Supported formats**: JPG, JPEG, PNG
- **Language support**: English (configurable in `easyocr_helper.py`)
- **Automatic text extraction**: Uploaded images are processed automatically
- **Integration**: OCR text becomes chat input seamlessly

## 💾 Chat Management

- **Auto-save**: Conversations are automatically saved
- **Search functionality**: Find specific chats by title
- **Recent chats**: Quick access to last 5 conversations
- **New chat**: Start fresh conversations anytime

## 🔍 Search Functionality

Use the sidebar search feature to:
- Find conversations by keywords
- Filter through chat history
- Quick access to relevant discussions

## 🚨 Error Handling

The application includes comprehensive error handling for:
- Missing API keys
- Model availability issues
- OCR processing errors
- Network connectivity problems

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📋 Requirements

Create a `requirements.txt` file with the following dependencies:

```txt
streamlit>=1.28.0
ollama>=0.1.7
openai>=1.3.0
easyocr>=1.7.0
pillow>=9.0.0
```

## 🐛 Troubleshooting

### Common Issues

1. **Ollama not responding**
   - Ensure Ollama service is running: `ollama serve`
   - Check if models are pulled: `ollama list`

2. **DeepSeek API errors**
   - Verify API key is set correctly
   - Check API quota and usage limits

3. **OCR not working**
   - Ensure image file is not corrupted
   - Check supported file formats (JPG, JPEG, PNG)

4. **Memory issues**
   - Use smaller models for limited resources
   - Close other applications consuming memory

## 🙏 Acknowledgments

- [Ollama](https://ollama.ai/) for local LLM serving
- [DeepSeek](https://www.deepseek.com/) for cloud API services
- [EasyOCR](https://github.com/JaidedAI/EasyOCR) for OCR capabilities
- [Streamlit](https://streamlit.io/) for the web framework

---

**Made with ❤️ using Streamlit, Ollama, and DeepSeek**