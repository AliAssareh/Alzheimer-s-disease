# Alzheimer's Disease Prediction

This project utilizes data from the Alzheimer's Disease Neuroimaging Initiative (ADNI), including 3D MRI and PET scans, to classify patients with either mild cognitive impairment or early stages of Alzheimer's disease using deep learning (CNN networks). For patients without PET scans, a CycleGAN network enhanced with spatial and channel attention mechanisms is used to impute PET images from their MRI scans. This approach ensures that both MRI and PET images are available for all patients, leading to a 7% improvement in classification accuracy compared to the work of R. Li et al. in “Deep Learning Based Imaging Data Completion for Improved Brain Disease Diagnosis,” 2014, pp. 305–312. doi: 10.1007/978-3-319-10443-0_39.

## Features
- CycleGAN model enhanced with spatial and channel attention mechanisms to impute missing PET images.
- Classification model utilizing both MRI and PET images, achieving a 79% accuracy.
- Comparison with MRI-only classification accuracy (69%).

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/AliAssareh/Alzheimers-disease-prediction.git
    cd Alzheimers-disease-prediction
    ```
2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
3. Obtain the dataset from ADNI (contact me or visit the ADNI website for data access).

## Usage
To regenerate the results, follow these steps:
1. Preprocess the input data:
    ```bash
    jupyter notebook preprocessing.ipynb
    ```
2. Train the CycleGAN model to impute the missing PET images from MRI scans:
    ```bash
    jupyter notebook cyclegan.ipynb
    ```
3. Train the proposed classifier for patient classification:
    ```bash
    jupyter notebook classification.ipynb
    ```
4. (Optional) Train a classifier relying solely on MRI images (accuracy: 69%):
    ```bash
    jupyter notebook MRI-classifier.ipynb
    ```

## Contributing
To contribute to this project, please:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

I appreciate any suggestions or contributions to improve this project.

## License
The project is licensed under the [MIT License](LICENSE). Note that the work is in progress and will soon be published in a journal paper. Please do not use this work for publishing your own papers before the official publication.

## Contact
For any questions or inquiries, please contact me at assareh73@gmail.com.

## Screenshots/Examples
- ROC curve of the classifier:

![ROC Curve](https://github.com/AliAssareh/Alzheimer-s-disease/blob/main/roc_curve.png)

- Comparison of the produced PET scan and the real PET scan of the patient:

![PET Scan Comparison](https://github.com/AliAssareh/Alzheimer-s-disease/blob/main/pet_scan_comparison.png)


## Technologies Used
- Python (TensorFlow)
- Jupyter Notebook

## Future Plans
I plan to improve the accuracy of the classifier by applying new models and methods.

