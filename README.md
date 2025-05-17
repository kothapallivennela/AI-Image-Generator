# AI-Image-Generator
Generate AI images from text prompts using a simple frontend interface.


🧠 Introduction
This project is an AI Image Generator built using HTML, CSS, and JavaScript, integrated with the OpenAI API. It allows users to input a text prompt and generate a set of AI-created images based on their description. The generated images are displayed in an elegant gallery format, each with an option to download directly.

The application opens with a dedicated section featuring a clear heading and a descriptive paragraph to guide users. A clean and intuitive form enables users to:

Enter a text prompt.

Select the number of images they want to generate via a dropdown.

Trigger image generation with a submit button.

A responsive loading state provides real-time feedback during processing. Once complete, the resulting images are presented in styled cards within the gallery, each accompanied by a download button for user convenience.

⚙️ How It Works
🔧 HTML Structure
The UI is divided into two main sections:

A form section for collecting user input (image description and quantity).

A gallery section to display the generated images.

🧠 JavaScript Logic
The application uses JavaScript and the Fetch API to send a POST request to the OpenAI Image Generation API.

The response is parsed and used to update the gallery with newly generated images.

The OpenAI API key is stored in a constant (OPENAI_API_KEY). Ensure your API key is kept secure — using server-side handling is recommended for production use.

🔁 Core Functions
generateAiImages()
An asynchronous function that:

Takes the user input (prompt and number of images).

Sends a request to OpenAI.

Receives and processes the image data.

Calls a function to update the UI with the results.

updateImageCard()
This function:

Iterates through the image array.

Updates image elements in the gallery with base64-encoded data.

Adds download functionality to each image card.

Form Event Handling
The default form submission behavior is prevented.

User input is captured.

A loading animation is shown during processing.

The generateAiImages() function is called to fetch and display the results.
