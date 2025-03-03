## About the project
This project is a comprehensive AI-based career assistant designed to help users explore potential career options based on their interests, goals, and aspirations. The assistant provides career advice in a friendly and concise manner and leverages external tools to enhance the interaction. For example, after suggesting suitable career paths, it can retrieve the average cost of studying at a specified university and even generate a visual representation of a student at that institution using DALL-E 3.

Key features include:

- **Natural Language Processing:** Uses OpenAI’s GPT models to analyze user input and generate context-aware career suggestions.
- **Tool Integration:** Supports function calls (tool calls) to fetch additional information such as the average tuition cost of universities.
- **Image Generation:** Uses DALL-E 3 to create vibrant pop-art style images that represent students in their respective universities.
- **Text-to-Speech:** Converts the assistant’s text responses into audio using OpenAI’s TTS model, providing an engaging multimodal interaction.
- **Real-Time Streaming:** Implements a streaming chat function to display responses as they are generated, ensuring a smooth user experience.
- **Web Interface:** Built with Gradio, the project features an interactive web UI where users can converse with the assistant, view generated images, and listen to the audio output.

This project demonstrates how to integrate multiple modalities (text, images, audio) with function calling capabilities to build a more interactive and informative AI assistant. It is ideal for users interested in exploring career options and associated educational costs through a rich, multimodal interface.

## Features
- **Career Guidance:** Analyze user goals to suggest career paths.
- **University Cost Lookup:** Fetch average tuition costs for various universities using integrated tool calls.
- **Image Generation:** Create custom images that visually represent university experiences.
- **Audio Feedback:** Convert text responses to speech for a hands-free experience.
- **Interactive UI:** A clean and responsive interface built with Gradio.
- **Streaming Responses:** Real-time incremental display of AI responses.

## Requirements
- Python 3.7 or later
- [OpenAI Python Library](https://github.com/openai/openai-python)
- [Gradio](https://gradio.app/)
- [python-dotenv](https://pypi.org/project/python-dotenv/)
- [Pillow](https://pillow.readthedocs.io/en/stable/)
- Additional libraries: `json`, `base64`, `io`

## Installation
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Abdulllah-Rizwan/Multimodal-Ai-Career-Assistant.git
   cd Multimodal-Ai-Career-Assistant
   ```
2. **Create a Virtual Environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use: venv\\Scripts\\activate
   ```
3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
4. **Set Up Environment Variables:**
   Create a `.env` file in the project root and add your OpenAI API key:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   ```

## Usage
1. **Run the Application:**
   ```bash
   python app.py
   ```
2. **Interact with the Assistant:**
   - Open the provided local URL in your browser.
   - Type your message into the textbox to start a conversation with the AI assistant.
   - The assistant will respond by suggesting career options and, if applicable, provide additional details such as average university costs. It will also generate images and audio output as part of the interaction.

## Code Structure
- **app.py:** Main application file containing the logic for setting up the chat interface, processing tool calls, streaming responses, and integrating image/audio functionalities.
- **Functions:**
  - `get_avg_university_cost`: Retrieves average tuition fees for a given university.
  - `handle_tool_calls`: Processes tool call data received from OpenAI and returns relevant information.
  - `artist`: Generates an image based on the provided university name using DALL-E 3.
  - `talker`: Converts text responses to speech using OpenAI’s TTS model.
  - `chat`: Manages the conversation flow, handling streaming responses, tool calls, and updating the conversation history.
- **UI:** Constructed with Gradio, allowing users to interact with the assistant via a web interface.

## Contributing
Contributions are welcome! Feel free to fork the repository, create new branches for features or bug fixes, and open pull requests.

## License
This project is licensed under the [MIT License](LICENSE).
