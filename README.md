# Metal Defect Identification and Classification

This repository contains the research and implementation for an automated metal defect detection system. The project compares four popular machine learning models—**K-Nearest Neighbors (KNN)**, **Support Vector Machine (SVM)**, **Naïve Bayes**, and **Random Forest**—to identify and classify defects in metal surfaces. The work was carried out as part of research at the AIML Department, Symbiosis Institute of Technology, Pune, India.

## Table of Contents

- [Overview](#overview)
- [Project Motivation](#project-motivation)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Conclusion](#conclusion)
- [References](#references)
- [Usage](#usage)
- [License](#license)

## Overview

Metal surface defect detection is a crucial component in modern industrial quality control. Traditional methods have given way to automated approaches using machine learning, which offer high accuracy and cost-effective solutions. This project focuses on detecting four types of metal defects: **corrosion**, **crack**, **dent**, and **no damage**.

## Project Motivation

- **Safety and Efficiency:** Improve quality control and reduce the risk of accidents by early detection of defects.
- **Cost-Effective:** Provide an automated, low-resource alternative to manual inspection, eliminating the need for expensive equipment.
- **Versatility:** Apply the solution across different metal types and defect categories.

## Dataset

A custom dataset was created combining web-scraped images and hand-captured photographs. It includes:
- **588 images** divided into four classes:
  - **Corrosion:** 150 images
  - **Crack:** 158 images
  - **Dent:** 145 images
  - **No Damage:** 135 images
- **Preprocessing:** All images were converted to grayscale and resized to 256×256 pixels. Additional enhancements like Gaussian Blur and Histogram Equalisation were applied to improve model accuracy.

## Methodology

The project workflow includes:
1. **Dataset Creation:** Images from seven commonly used industrial metals (Aluminium, Bronze, Copper, Iron, Stainless Steel, Steel, Nickel) were collected.
2. **Data Preprocessing:** Implementing techniques such as image grayscaling, resizing, Gaussian Blur, and Histogram Equalisation.
3. **Model Training & Testing:** Four machine learning models were trained using the preprocessed dataset.
4. **Comparative Analysis:** Models were evaluated based on accuracy, precision, recall, and F1-score. The KNN model delivered the best performance.
5. **Deployment:** The final model was deployed using Streamlit for real-time defect detection.

## Results

The following table summarizes the performance of the models before and after applying preprocessing techniques:

| Model         | Accuracy Before Preprocessing | Accuracy After Preprocessing | Best Result |
|---------------|-------------------------------|------------------------------|-------------|
| **KNN**       | 0.5677                        | 0.9269                       | **0.9269**  |
| **SVM**       | 0.7033                        | 0.7582                       | 0.7582      |
| **Naïve Bayes** | 0.4576                      | 0.5114                       | 0.5114      |
| **Random Forest** | 0.6075                    | 0.7454                       | 0.7454      |

Detailed results and evaluation metrics (precision, recall, F1-score) are included within the full research paper.

## Conclusion

The comparative analysis confirms that the KNN model is best suited for this defect detection application with the highest accuracy after preprocessing. The project presents a non-invasive, resource-efficient tool for real-time metal defect detection that could significantly improve quality control in various industrial settings.

## References

1. [Investopedia – Metals and Mining Sector](https://www.investopedia.com/ask/answers/040615/what-metals-and-mining-sector.asp)
2. [Nature – Effective Detection of Metal Surface Defects](https://www.nature.com/articles/s41598-023-47716-2)
3. [Maryland Injury Lawyer – Manufacturing Defects](https://www.marylandinjurylawyer.net/road-accidents-resulting-from-manufacturing-defects.html)
4. [Pipeline Corrosion – DD Coatings](https://www.ddcoatings.co.uk/2515/what-is-pipeline-corrosion)
5. [Towards Data Science – Top Machine Learning Models](https://towardsdatascience.com/top-machine-learning-algorithms-for-classification-2197870ff501)

For a detailed literature review, please refer to the [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1LFkYGb7sUtqKRUkDqQ5ReAwl1tcjj3a4fW7jRXldg-o/edit?usp=sharing).

## Usage

To replicate this work:
1. Clone this repository.
2. Install the required libraries (e.g., scikit-learn, Streamlit, OpenCV).
3. Run the preprocessing and training scripts.
4. Use the provided Streamlit app to deploy the defect detection model in real time.

```bash
git clone <repository-url>
cd <repository-folder>
pip install -r requirements.txt
streamlit run app.py
