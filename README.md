# 🎙️ Terminal Voice Assistant (TVA)

A voice-activated AI assistant that runs directly in your terminal. Talk to your terminal, get intelligent responses, and execute commands hands-free.

![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-in%20development-orange.svg)

## ✨ Features

- 🎤 **Voice Control** - Speak naturally to your terminal
- 🤖 **AI-Powered** - Uses Claude API for intelligent responses
- 🎯 **Terminal-First** - Designed specifically for command-line workflows
- 🔊 **Multiple Modes** - Push-to-talk, wake word, or continuous listening
- 🛡️ **Safe Execution** - Confirms before running potentially dangerous commands
- 🚀 **Fast & Local** - Speech recognition runs entirely on your machine

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/terminal-voice-assistant.git
cd terminal-voice-assistant

# Install dependencies
pip install -r requirements.txt

# Set up your API key
echo "ANTHROPIC_API_KEY=your-key-here" > .env

# Run the assistant
python src/main.py
```

## 📋 Prerequisites

- Python 3.9 or higher
- Claude API key from [Anthropic](https://console.anthropic.com/)
- Working microphone
- macOS, Linux, or Windows

## 💬 Usage

Once running, the assistant listens for your voice input:

```bash
# Press and hold SPACEBAR to talk (default)
[LISTENING] ● Press SPACE to talk...

# Examples of what you can say:
"What files are in this directory?"
"Show me the current git status"
"How do I compress these files?"
"Create a Python script called test.py"
"Explain this error message..."
```

### Voice Commands Examples

- **File Operations**: "List all Python files", "Create a new folder called docs"
- **Git Commands**: "What's my git status?", "Show recent commits"
- **System Info**: "Check disk space", "What processes are running?"
- **Coding Help**: "Write a function to parse JSON", "Explain this regex"
- **General Questions**: "How do I use grep?", "What's the syntax for a bash loop?"

## ⚙️ Configuration

Edit `config/config.yaml` to customize:

```yaml
audio:
  mode: "push_to_talk"  # or "wake_word", "continuous"
  wake_word: "hey terminal"
  
whisper:
  model_size: "base"  # tiny, base, small, medium, large
  
claude:
  model: "claude-3-opus-20240229"
  max_tokens: 1000
```

## 🏗️ Project Structure

```
terminal-voice-assistant/
├── src/
│   ├── main.py           # Main application
│   ├── audio/            # Voice recording & transcription
│   ├── ai/               # Claude API integration
│   └── terminal/         # Terminal interface
├── config/               # Configuration files
├── requirements.txt      # Python dependencies
└── README.md            # You are here
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Todo

- [ ] Basic voice recording and transcription
- [ ] Claude API integration
- [ ] Terminal UI with status indicators
- [ ] Command execution with safety checks
- [ ] Wake word detection
- [ ] Custom voice commands
- [ ] Session history and context
- [ ] Multi-language support

## 🔧 Troubleshooting

**No audio input detected**

- Check your microphone permissions
- Verify your audio input device: `python -m sounddevice`

**Whisper model download issues**

- Models are downloaded to `~/.cache/whisper`
- Try manually downloading: `python -c "import whisper; whisper.load_model('base')"`

**API errors**

- Verify your ANTHROPIC_API_KEY in `.env`
- Check your API usage limits at [console.anthropic.com](https://console.anthropic.com)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenAI Whisper](https://github.com/openai/whisper) for speech recognition
- [Anthropic Claude](https://www.anthropic.com/) for AI responses
- [Rich](https://github.com/Textualize/rich) for beautiful terminal formatting

## 🔗 Links

- [Documentation](docs/)
- [Issue Tracker](https://github.com/yourusername/terminal-voice-assistant/issues)
- [Discussions](https://github.com/yourusername/terminal-voice-assistant/discussions)

---

**Note**: This project is under active development. Features and APIs may change.

Made with ❤️ for developers who prefer talking to typing
