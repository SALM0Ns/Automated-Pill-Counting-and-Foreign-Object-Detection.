## The Research are in process...

Research Proposal: Automated Pill Counting and Foreign Object Detection Using Image Processing and Machine Learning
Advisor: Dr. Warattapop Thapatsuwan, Ph.D., Department of Computer Science, Kasetsart University

1. Introduction and Background

In the pharmaceutical industry and hospital pharmacy units, manual pill counting and inspection remain error-prone and time-consuming. These processes are not only labor-intensive but also prone to human error, leading to miscounts or overlooked contamination, especially in high-volume settings. With the advancement of computer vision and machine learning, there is an opportunity to automate these tasks efficiently. This proposal outlines the development of a system that can automatically count pills and detect foreign objects using image processing techniques and data-driven methods.

2. Problem Statement

Manual pill counting is inefficient and unreliable, particularly when pills overlap or are partially occluded. Additionally, foreign objects such as plastic fragments, paper dust, or other unexpected contaminants are difficult to detect by the naked eye, especially under high-speed workflows. A solution is needed to accurately count and validate pill presence and quality without relying on human supervision.

3. Research Objectives
	•	To develop an image preprocessing pipeline that enhances pill visibility and edge detection.
	•	To implement an automated pill counting algorithm based on image contour analysis.
	•	To identify and flag foreign objects that deviate from pill properties using shape, size, or intensity.
	•	To apply advanced data augmentation strategies to synthesize realistic pill tray scenarios.
	•	To build a foundation for training deep learning models on synthetic and real-world datasets.

4. Methodology

4.1 Data Acquisition and Preprocessing

Images of pills are captured on a black background using a controlled lighting environment. Preprocessing includes:
	•	Grayscale Conversion to simplify color channels.
	•	CLAHE (Contrast Limited Adaptive Histogram Equalization) to enhance local contrast.
	•	Shannon Entropy Thresholding for adaptive binarization.
	•	Canny Edge Detection to extract pill boundaries.
	•	Morphological Operations to remove noise and close broken contours.

4.2 Data Augmentation

Inspired by Daus et al. (2022), the dataset is expanded using a copy-paste augmentation strategy, which involves:
	•	Random rotation (0–360°) per pill to simulate real scatter.
	•	Random scaling within a defined range to simulate size variation.
	•	Random spacing and position to model different pill densities.
	•	Occlusion and truncation by overlapping pills and placing pills at the edge of the scene.
	•	Defocus simulation by blurring selected pills to represent out-of-focus regions.

These augmentations aim to prevent overfitting, increase generalization, and mimic real-world pill scattering conditions.

4.3 Pill Counting and Foreign Object Detection

Contour detection is used to localize pill-like objects. Filters based on size, shape ratio, and roundness help distinguish pills from noise or foreign objects. In the final phase, machine learning or deep learning classifiers may be introduced to further enhance detection and classification performance.

5. Expected Outcomes
	•	A functional and scalable preprocessing pipeline suitable for integration with machine learning models.
	•	A realistic synthetic dataset with annotated pills and contaminants.
	•	Preliminary object detection and counting models trained on synthetic data.
	•	A proof-of-concept system capable of operating in semi-automated pill verification pipelines.

6. Significance

This research provides a cost-effective, scalable solution for automated pill counting and contamination detection, enhancing quality control in pharmaceutical and clinical settings. The use of synthetic data through domain-specific augmentation reduces dependency on labor-intensive data labeling, enabling faster model development and deployment.

