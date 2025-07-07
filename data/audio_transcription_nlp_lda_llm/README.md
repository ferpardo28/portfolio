# Audio Transcription NLP LDA LLM

This project demonstrates how to extract meaningful insights from audio files using a Natural Language Processing (NLP) pipeline that includes:

- Automatic transcription using Whisper (OpenAI API)
- Text cleaning and preprocessing
- Keyword extraction using LDA (Latent Dirichlet Allocation)
- Summary and subtopic generation using a Large Language Model (LLM)

## Project Structure

### Audio Download and Processing
Audio fables are downloaded from Project Gutenberg and analyzed using librosa to verify duration and integrity.

### Transcription
Audio files are transcribed using OpenAI's Whisper model.

### Text Cleaning
The transcriptions are cleaned using regex-based functions and stopword removal.

### Keyword Extraction
LDA is applied to extract key topic words from each transcription.

### Summary Generation with LLM
Keywords are used as input to GPT to generate a short summary and subtopics per fable.

## Technologies Used

- Python
- OpenAI API (Whisper + GPT)
- Gensim
- NLTK
- Librosa

## File

- `audio_transcription_nlp_lda_llm.ipynb`: Main notebook with all code and explanations.

## Reflections

This project highlights the power of combining audio transcription with topic modeling and language generation tools to extract structured insights from unstructured audio content.
