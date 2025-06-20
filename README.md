# Crop Classification using Sentinel-2 and Random Forest

This project uses Google Earth Engine and Sentinel-2 imagery to classify agricultural land into Corn, Soybeans, and Fallow using a Random Forest classifier.

## Tools & Libraries
- Google Earth Engine Python API
- geemap
- Sentinel-2 SR data
- Random Forest classifier

## Setup
1. Install dependencies: `pip install -r requirements.txt`
2. Authenticate with GEE using `earthengine authenticate`
3. Run the script `crop_classifier.py`

## Output
- Classified crop map
- Accuracy metrics
