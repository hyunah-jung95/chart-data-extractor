# Chart Data Extractor
https://github.com/user-attachments/assets/cc043d67-6d00-4017-9c19-03dc8bac9b4c

# User Flow
1. Upload an impage file
2. Gemini-Flash automatically extracts the data

# Technical Considerations
## Streamlit and VertexAI Integration
- Handling the integration between the Streamlit file uploader widget and the VertexAI API posed a challenge, as detailed below:
  - The Streamlit file uploader stores the uploaded file as a 'file-like' object.
  - To interact with the VertexAI API, this object must be converted into a byte stream using the `uploaded_file.getvalue()` method.
  - The byte stream is then passed to the VertexAI API, where it is converted into an image format compatible with VertexAI using the `vertexai.generative_models.Image.from_bytes()` method.
## Gemini Flash vs. Pro:
- After comparing the Gemini Flash and Pro versions in terms of performance and cost, we chose to proceed with the Flash version due to its optimized balance of both.

# Tech Stacks
- Streamlit
- Python
- VertexAI APIs
- GCP SDK
