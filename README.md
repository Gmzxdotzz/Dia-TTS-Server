# Dia TTS Server 🌟

![Dia TTS Server](https://img.shields.io/badge/version-1.0.0-blue.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg) ![Stars](https://img.shields.io/github/stars/Gmzxdotzz/Dia-TTS-Server.svg) ![Forks](https://img.shields.io/github/forks/Gmzxdotzz/Dia-TTS-Server.svg)

Welcome to the **Dia TTS Server**! This repository allows you to self-host the powerful Dia TTS model, providing a seamless experience for text-to-speech applications. With a user-friendly web interface and flexible API endpoints, you can easily integrate this tool into your projects.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Voice Cloning](#voice-cloning)
- [Dialogue Generation](#dialogue-generation)
- [Execution on GPU/CPU](#execution-on-gpu-cpu)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Features ✨

- **User-Friendly Web UI**: Navigate easily through a clean and intuitive interface.
- **Flexible API Endpoints**: Supports OpenAI compatible endpoints for easy integration.
- **Support for SafeTensors/BF16**: Optimized for better performance and efficiency.
- **Voice Cloning**: Create unique voices tailored to your needs.
- **Dialogue Generation**: Generate realistic conversations for various applications.
- **GPU/CPU Execution**: Choose your preferred execution environment for optimal performance.

## Getting Started 🚀

To get started with the Dia TTS Server, follow these steps:

1. **Clone the Repository**: Use the command below to clone the repository to your local machine.

   ```bash
   git clone https://github.com/Gmzxdotzz/Dia-TTS-Server.git
   ```

2. **Navigate to the Directory**: Change to the project directory.

   ```bash
   cd Dia-TTS-Server
   ```

3. **Install Dependencies**: Install the required packages.

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Server**: Start the server using the command below.

   ```bash
   python main.py
   ```

5. **Access the Web UI**: Open your browser and navigate to `http://localhost:8000`.

## Installation 🛠️

### Prerequisites

- Python 3.7 or higher
- Pip
- Git
- CUDA (for GPU execution)

### Steps

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Gmzxdotzz/Dia-TTS-Server.git
   ```

2. **Install Python Packages**:

   Navigate to the cloned directory and run:

   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Environment**:

   Set up any necessary environment variables as outlined in the `config.py` file.

4. **Run the Application**:

   Execute the following command:

   ```bash
   python main.py
   ```

## Usage 📖

Once the server is running, you can interact with the web UI or use the API endpoints.

### Web UI

Access the web interface by visiting `http://localhost:8000` in your web browser. You can input text and generate speech directly from the UI.

### API Endpoints

The server provides several API endpoints for integration into your applications. Here are some key endpoints:

- **Generate Speech**: POST request to `/api/generate` with text data.
- **Clone Voice**: POST request to `/api/clone` with voice samples.
- **Dialogue Generation**: POST request to `/api/dialogue` with conversation context.

## API Endpoints 🔗

### Generate Speech

**Endpoint**: `/api/generate`

**Method**: POST

**Request Body**:

```json
{
  "text": "Your text here",
  "voice": "selected_voice"
}
```

**Response**:

```json
{
  "audio_url": "URL_to_generated_audio"
}
```

### Clone Voice

**Endpoint**: `/api/clone`

**Method**: POST

**Request Body**:

```json
{
  "voice_samples": ["sample1.wav", "sample2.wav"]
}
```

**Response**:

```json
{
  "voice_id": "unique_voice_id"
}
```

### Dialogue Generation

**Endpoint**: `/api/dialogue`

**Method**: POST

**Request Body**:

```json
{
  "context": "previous conversation context"
}
```

**Response**:

```json
{
  "dialogue": "Generated dialogue response"
}
```

## Voice Cloning 🗣️

Voice cloning allows you to create custom voices based on provided samples. To clone a voice:

1. Collect audio samples of the desired voice.
2. Send a POST request to the `/api/clone` endpoint with the audio files.

The server will process the samples and return a unique voice ID that you can use for generating speech.

## Dialogue Generation 💬

The dialogue generation feature enables you to create realistic conversations. You can provide a context, and the server will generate responses that fit naturally within that context.

To use this feature:

1. Prepare the conversation context.
2. Send a POST request to the `/api/dialogue` endpoint.

## Execution on GPU/CPU ⚙️

The Dia TTS Server supports execution on both GPU and CPU. You can choose your preferred execution environment by configuring the settings in the `config.py` file.

### GPU Execution

To enable GPU execution, ensure you have the appropriate CUDA drivers installed. The server will automatically detect the GPU and utilize it for processing.

### CPU Execution

If you prefer to run on CPU, simply set the configuration to use CPU. The server will adjust its processing accordingly.

## Contributing 🤝

We welcome contributions from the community! If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your forked repository.
5. Create a pull request.

Please ensure that your code adheres to the existing style and includes appropriate tests.

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links 🔗

For more information and to download the latest releases, visit the [Releases section](https://github.com/Gmzxdotzz/Dia-TTS-Server/releases). Check back often for updates and new features!

## Conclusion

Thank you for checking out the Dia TTS Server! We hope you find it useful for your text-to-speech applications. If you have any questions or feedback, feel free to open an issue in the repository.

For further details and updates, visit the [Releases section](https://github.com/Gmzxdotzz/Dia-TTS-Server/releases). Enjoy your experience with Dia TTS!