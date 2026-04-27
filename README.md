# Skin Lesion Image Analysis
Use this repository as a guide for the creation of your own repository and presentation.

## Context of the Project
In this project, you are stepping into the role of a Junior Data Scientist at a health-tech startup. You are tasked with addressing a critical gap in dermatological care: the automated detection of skin cancer. Using the*MILK10k dataset, you will build a Deep Learning system capable of classifying images into either binary (Benign vs. Malignant) or 11 distinct diagnostic categories. Your primary goal is to determine if you can improve diagnostic accuracy by combining dermatoscopic images with patient metadata, such as age, sex, and lesion site, using a multimodal model.

## Necessary Software
To complete this analysis, you will need to set up a Python environment with the following libraries:
*   **Python 3.8+**: The foundational language for the project.
*   **PyTorch & Torchvision**: To build and train your neural networks.
*   **timm (PyTorch Image Models)**: To access pretrained state-of-the-art architectures like EfficientNet.
*   **Pandas & NumPy**: To clean your metadata and handle numerical arrays.
*   **Scikit-learn**: To calculate your One-vs-Rest (OvR) AUC scores and generate classification reports.
*   **Matplotlib & Seaborn**: To visualize your training curves and confusion matrices.

## Documentation Map
Refer to the following files in this repository to navigate your workflow:
*   **`/DATA`**: Contains your ground truth labels, metadata, and instructions for acquiring the full image set.
*   **`/PROJECT_MATERIALS`**: Contains the essential resources to succeed, including the Project Hook, the evaluation Rubric, academic articles for deeper understanding, and an example presentation.
*   **`/SCRIPT_TEMPLATES`**: These are your primary resources, containing code for both binary and 11-class models, covering image-only and multimodal approaches.
*   **`README.md`**: Your central hub for project setup.

## Step-by-step Instructions

1.  **Repository Setup**: Create your own GitHub repository for this case study. You will use this space to compile your completed scripts, any cleaned datasets you generate, and your final output files.
2.  **Data Acquisition**: Head to the `/DATA` folder and follow the guide in `How_to_Acquire_Images.md` to link the image files to your workspace.
3.  **Exploratory Data Analysis (EDA)**: Before coding your model, perform an EDA. Analyze the distribution of the 11 categories and binary labels to understand class imbalances and explore relationships within the patient metadata.
4.  **Metadata Cleaning**: Open your chosen templates from `/SCRIPT_TEMPLATES/`. Perform data imputation (e.g., filling in missing ages) and one-hot encoding for categorical variables like sex or site. Save any resulting cleaned datasets to your repository.
5.  **Model Implementation**: Use the provided templates to build your models. It is preferred that you complete all four templates; however, you may choose to complete either both 11-class templates or both binary templates. Choose a backbone from the `timm` library (such as `efficientnet_b0`) and implement the training loop, ensuring you freeze the backbone for initial head training before full fine-tuning.
6.  **Statistical Testing**: After training, conduct statistical tests to compare the performance of your models. For example, use tests to determine if the inclusion of metadata in the multimodal approach provides a statistically significant improvement in AUC or Accuracy over the image-only approach.
7.  **Analysis and Output**: Execute your scripts and save the results. You must generate and save a confusion matrix and training curves (Loss, Accuracy, AUC) for each model to your repository.
8.  **Final Presentation**: Using your EDA findings, model results, statistical analysis, and visualizations, create a final presentation. Add this presentation (in PDF or slide format) to your repository to complete the case study.

## References
[1] M. Tan and Q. V. Le, "EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks," arXiv.org, 2019. [Online]. Available: https://arxiv.org/abs/1905.11946. [Accessed: Apr. 27, 2026].

[2] "The ISIC Archive," International Skin Imaging Collaboration, 2026. [Online]. Available: https://www.isic-archive.com/. [Accessed: Apr. 27, 2026].

[3] "Getting Started with PyTorch Image Models (timm)," Hugging Face, 2026. [Online]. Available: https://huggingface.co/docs/timm/quickstart. [Accessed: Apr. 27, 2026].

[4] "PyTorch Documentation," PyTorch.org, 2026. [Online]. Available: https://pytorch.org/docs/stable/index.html. [Accessed: Apr. 27, 2026].

[5] J. Streifer and M. S. Palmer, "The Case Study Method in Data Science Education," University of Virginia CTE, 2020. [Online]. Available: https://cte.virginia.edu/. [Accessed: Apr. 27, 2026].
