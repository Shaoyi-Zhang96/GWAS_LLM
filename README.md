# SNP-Disease Association Analysis

## Overview
This project provides a comprehensive pipeline for analyzing SNP-disease associations. The script extracts relevant information from PubMed, NCBI Gene database, and web search results to provide structured insights into biomedical relationships.

## Features
- **PubMed Article Retrieval**: Searches PubMed for relevant scientific literature.
- **SNP Information Lookup**: Retrieves SNP details from NCBI Gene.
- **Web Search Integration**: Fetches additional context from general web searches.
- **Abstract Extraction**: Extracts abstracts from PubMed articles.
- **Automated Analysis**: Summarizes associations between SNPs and diseases.
- **Batch Processing**: Processes multiple SNP-disease pairs from an input file.
- **Structured Output**: Generates CSV summaries for easy review.

## Requirements
The script requires the following Python packages:
- `requests`
- `beautifulsoup4`
- `lxml`
- `csv`
- `json`
- `openai`

Ensure these dependencies are installed before running the script:
```sh
pip install requests beautifulsoup4 lxml openai
```

## Setup
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/snp-disease-analysis.git
   cd snp-disease-analysis
   ```
2. Replace `your api key` with your OpenAI API key in the script.
3. Run the script for batch processing:
   ```sh
   python script.py input_file.csv
   ```
   or for directory-based analysis:
   ```sh
   python script.py path/to/association/results/
   ```

## Input Format
The input file should be a txt (tab-separated) with the following structure:
```
SNP Disease
rs12345 Type 2 Diabetes
rs67890 Alzheimer's Disease
```

## Output
The results will be saved in the `snp_disease_results/` directory, with:
- **Individual reports**: Text files with analysis details for each SNP-disease pair.
- **Summary CSV**: `association_summary.csv` containing structured insights.

## Example Output CSV
| SNP | Disease | Association | Confidence | Genes | Pathways | Functional Impact |
|------|---------|-------------|------------|--------|-----------|-------------------|
| rs12345 | Type 2 Diabetes | Yes | High | TCF7L2 | Glucose Metabolism | Regulatory Variant |
| rs67890 | Alzheimer's Disease | Yes | Medium | APOE | Neurodegeneration | Missense Mutation |


## Contributors
- Shaoyi Zhang

