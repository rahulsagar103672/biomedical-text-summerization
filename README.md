# biomedical-text-summerization

# Biomedical Text Summarization Project

## Overview
This project focuses on summarizing biomedical research articles and translating the summaries into multiple Indian languages (Telugu, Hindi, and Tamil). The implementation includes web scraping, text processing, extractive summarization using frequency-based methods, and machine translation.

## Features
- Web scraping of biomedical articles from BMC Nephrology
- Text preprocessing and cleaning
- Extractive summarization using word frequency analysis
- Multi-language translation (English to Telugu, Hindi, Tamil)
- ROUGE metric evaluation capability (though not implemented in this notebook)

## Requirements
- Python 3.x
- Required Python packages:
  - beautifulsoup4
  - lxml
  - nltk
  - googletrans (version 4.0.0-rc1)
  - rouge

## Installation
1. Clone this repository
2. Install the required packages:
```bash
pip install beautifulsoup4 lxml nltk rouge
pip install googletrans==4.0.0-rc1
```

3. Download NLTK data:
```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
```

## Usage
1. Run the Jupyter notebook `BIOMEDICAL_TEXT_SUMMARIZATION_FINAL.ipynb`
2. The notebook will:
   - Scrape a biomedical article from BMC Nephrology
   - Generate an English summary
   - Translate the summary to Telugu, Hindi, and Tamil
   - Display all versions of the summary

## Customization
To analyze a different article:
1. Change the URL in the scraping section to point to your desired article
2. Adjust the number of sentences in the summary by modifying the parameter in `heapq.nlargest()`

To add more languages:
1. Add additional language codes to the `languages` list in the translation section
2. Supported language codes can be found in the googletrans documentation

## Output
The program outputs:
1. The original English summary
2. Translated summaries in:
   - Telugu
   - Hindi
   - Tamil

## Limitations
- The summarization is extractive (selects existing sentences) rather than abstractive (generates new sentences)
- Translation quality depends on the googletrans API
- Web scraping may fail if the website structure changes

## Future Improvements
- Implement abstractive summarization using transformer models
- Add more sophisticated evaluation metrics
- Expand to more Indian languages
- Create a web interface for easier use

## License
This project is open source and available under the MIT License.
