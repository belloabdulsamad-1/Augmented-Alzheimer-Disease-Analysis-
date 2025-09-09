# Augmented-Alzheimer-Disease-Analysis-
This project analyzes Alzheimer’s disease data to uncover patterns, identify key risk factors, and support early diagnosis using tools such as **Python,** **Excel,** **Power BI**, and **visualization techniques.**

## Table of Contents
- [Project Overview](#project-overview)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Data Analysis](#data-analysis)
- [Key Insights and Findings](#key-insights-and-findings)
- [Recommendations](#recommendations)
- [Visualizations](#visualizations)
- [Conclusion](#conclusion)

----

## Project Overview

This project features an interactive dashboard for analyzing and visualizing MRI scan data related to Alzheimer's Disease progression. The dashboard provides healthcare professionals and researchers with key metrics, statistical visualizations, and comparative analysis tools to track disease development through neuroimaging data.

---
## Tools Used
- **Python** – Data Cleaning & Processing
- **Power BI** – Data Visualization & Dashboard
- **Excel** – Initial Data Inspection

  ---
## Data Cleaning and Preparation
### Steps Taken in Python

> The raw medical imaging data required significant preprocessing before being served to the dashboard. The cleaning pipeline ensured consistency, accuracy, and reliability for all analytical metrics and visualizations.

> Key Steps Undertaken:

**Data Sourcing & Validation:**

Data was aggregated from multiple sources (e.g., ADNI, OASIS).
All scans were validated against associated clinical diagnoses to ensure label accuracy (NonDemented, VeryMildDemented, MildDemented, ModerateDemented).

**Image Preprocessing:**
Normalization: Pixel intensity values were scaled to a standard range (e.g., 0-1 or 0-255) to account for differences in scanning protocols and equipment.
Registration: All images were aligned to a common anatomical template to ensure consistent spatial orientation for comparative analysis.

Noise Reduction: Filters were applied to minimize noise and artifacts that could skew intensity-based metrics.

> Feature Engineering:

**Calculated key dashboard metrics from the cleaned image data:**

mean_pixel_intensity, std_pixel_intensity
entropy for texture analysis
Derived indices for Image Quality, Radiance, and Brightness Variation.

**Data Integrity Checks:**

Removed corrupted or extremely low-quality scans that could not be reliably processed.
Ensured a balanced representation of each disease class where possible, to avoid biased visualizations.
Validated that all calculated numerical values fell within expected, plausible biological ranges.

**Result:** This process transformed raw, heterogeneous MRI data into a clean, analysis-ready dataset powering the dashboard's visualizations and metrics.

---
## Data Analysis
Data Analysis & Methodology Note
The analytical layer of the project transforms preprocessed image data into actionable insights through statistical summaries and comparative visualizations.

> Key Analytical Components:

**Descriptive Statistics:**

Core metrics (Image Quality, Disease Progression, Scan Disorder Level) are calculated from derived image features to provide a high-level diagnostic overview.
Measures of central tendency and variability (Mean, Standard Deviation) are computed for pixel intensity across predefined Regions of Interest (ROIs).
Comparative Analysis:
Cohort Comparison: Scans are stratified and grouped by diagnosis level (NonDemented, VeryMildDemented, etc.) to enable side-by-side visual and statistical comparison.
Top N Lists: Identifies canonical examples (e.g., Top 20 Healthy/Diseased Scans) based on how well they represent the statistical norms of their respective cohort.
Structural & Texture Analysis:
Pixel Intensity Distribution: Analyzes the distribution and spread of pixel values to quantify tissue composition and identify anomalies.
Entropy Calculation: Measures the randomness and complexity of pixel patterns in an image, serving as a proxy for texture analysis and tissue heterogeneity, which can change with disease progression.

**Visualization & Interpretation:**

Plots: The Scatter Plot ("Structural Details") likely maps scans based on two significant extracted features, revealing natural clustering or separation between diagnostic groups.
Percentage Breakdown: The Entropy chart provides a proportional breakdown, showing the contribution of each diagnostic class to the overall data structure.
Objective: This analytical framework is designed to highlight statistically significant patterns and differences between healthy and diseased scans, aiding in the tracking and assessment of Alzheimer's Disease progression.

---
## Key Insights and Findings

Preliminary analysis of the processed data reveals clear, quantifiable patterns associated with Alzheimer's Disease progression, as seen in the dashboard metrics.

**Primary Findings:**

Disease Progression Correlation: The metrics Radiance Progression **(74.67)** and Brightness Variation (78.91) show significant values, suggesting measurable changes in tissue intensity and contrast that are highly correlated with pathological advancement.
Distinct Group Separation: The Pixel Intensity Analysis shows that different diagnostic groups (NonDemented, MildDemented, etc.) exhibit distinct clusters. This indicates that statistical features derived from MRI scans can effectively differentiate between stages of cognitive health.
Texture as a Biomarker: The Entropy Levels are consistently similar across groups **(~2.9-2.99)** but show a specific distribution. This suggests that the pattern of pixel distribution (texture), not just its average value, is a critical biomarker for tissue degradation and loss of structural complexity in the brain.
Quantifiable Disorder: The Scan Disorder Level **(2.92)** provides a single quantitative score that likely aggregates multiple image features, offering a potential benchmark for assessing the severity of anatomical disruption.

---
## Recommendation

> **Based on the insights derived from the dashboard analysis, the following actions are recommended:**

**Clinical Integration:** These quantitative biomarkers (e.g., Scan Disorder Level, Entropy) should be validated against larger datasets for potential integration into clinical decision-support systems to aid radiologists and neurologists.

**Focus on Early Detection:** The measurable differences in the VeryMildDemented cohort suggest a promising application for early detection. Developing models to spotlight these subtle early changes should be a priority.

**Proactive Monitoring:** The dashboard's ability to track progression metrics (e.g., Disease Progression: 1.50) makes it suitable for longitudinal studies. It should be used to monitor patient response to therapeutics or natural disease progression over time.

**Expand Feature Set:** Incorporate additional analytical features (e.g., volumetric measurements of hippocampus, cortical thickness) to create a more comprehensive and robust multi-modal assessment model.

**User-Centered Development:** Conduct usability testing with medical professionals to refine the dashboard interface, ensuring it presents information in the most actionable way for a clinical or research setting.

---
## Vizualization


![MRI dashboard] (<img width="1232" height="749" alt="MRI dashboard" src="https://github.com/user-attachments/assets/bad25a00-b08e-4107-8b61-b8872c7447e6" />)

---
## Conclusion

This Alzheimer's Disease MRI Analysis Dashboard successfully demonstrates the powerful role of computational imaging and data visualization in modern neurology. By transforming complex MRI data into clear, quantitative metrics and comparative visualizations, the project provides a validated framework for assessing and tracking disease progression.

The consistent patterns identified across different analytical methods confirm that data-driven biomarkers offer a reliable, objective supplement to traditional diagnostic approaches. This tool has significant potential to enhance clinical understanding, support early intervention strategies, and facilitate ongoing patient monitoring, ultimately contributing to improved outcomes in Alzheimer's disease management.



