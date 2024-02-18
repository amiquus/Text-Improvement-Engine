# Text Improvement Engine

## Description
This Python project includes a script for suggestions of stard. It utilizes Natural Language Processing (NLP) techniques to match phrases in a text file to a set of standard terms, and it calculates similarity scores between these phrases.

## Technologies Used
- **Python**: Version 3.11
- **Libraries/Frameworks**:
  - `spacy`: For tokenization and sentence splitting.
  - `torch`: For handling tensor operations.
  - `transformers`: For leveraging pre-trained NLP models.

## Setup and Installation
### Prerequisites
- Python 3.11

### Installation Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/amiquus/Text-Improvement-Engine.git
   cd your-repo-name
   ```

2. **Running the Application**:
   Command-line usage example:
   ```bash
   python analyzer.py sample_text.txt 0.5
   ```
   `sample_text.txt` is your input text file located in the `input` folder , and `0.5` is the cosine similarity threshold used for the sentence similarity comparison. Consider increasing it if the number of results is too large and decreasing it it if the number of results is too small.  

## Usage
- The script reads a text file and a list of standardized terms, then finds and suggests terms from this list that closely match phrases in the text.
- It can be run from the command line with arguments for the text file path and an optional similarity threshold.

## Design Rationale
### Modular Design
- The project is structured into classes for readability and maintenance: `DataLoader` for file operations, `ModelHandler` for model management, and `TextProcessor` for processing logic.
- This separation of concerns makes the code easier to understand and modify.

### NLP Model Choice
- `all-MiniLM-L6-v2` is a lightweight sentence-transformers model: It maps sentences & paragraphs to a 384 dimensional dense vector space and can be used for tasks like clustering or semantic search. 
- `spacy` is used for its efficiency in text tokenization and sentence splitting.
- `transformers` and `torch` are used for their robustness and performance in handling NLP tasks.

### CLI Integration
- Implemented command-line interface functionality for easy and flexible use of the tool.
