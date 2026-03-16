# Image-in-Question Detector — Assessment Task

## Problem Statement
You are given a dataset of 19,633 exam questions (JEE/NEET) that were originally in image format (scanned PDFs) and converted to text using OCR.

Some of these questions originally contained **diagrams, figures, circuits, graphs, or other visual elements** that were lost during the OCR conversion. The text was extracted, but the images were not.

**Your task:** Build a system that identifies which questions originally had images/diagrams — using only the converted text data.

## Dataset
- **File:** `ocr_converted.jsonl`
- **Format:** One JSON object per line (JSONL)
- **Key fields per entry:**
  - `_id.$oid` — unique question identifier
  - `qtype` — question type (scq, mcq, integerQuestion, etc.)
  - `ocr_fields` — contains the converted text fields (question, solution, or both)
    - `ocr_text` — raw OCR text with LaTeX
    - `html` — converted MathML HTML
    - `image_count` — number of images in the original
    - `has_dead_images` — whether original image URLs are broken

## What to Deliver
1. A script/program that processes `ocr_converted.jsonl` and outputs a list of question IDs that likely had images/diagrams
2. A brief explanation of your approach
3. Your estimated accuracy and what your system catches vs what it might miss
4. Any creative methods you used beyond obvious keyword matching

## Rules
- You can use any programming language, AI tools, or libraries
- Time limit: 1 day
- Focus on **creativity** — anyone can grep for "figure" or "diagram". What else can you detect?

## Setup
```bash
git clone <this-repo-url>
cd ocr-image-text-analysis
# ocr_converted.jsonl is your input file
```
