# Hybrid Machine Learning Model for Early Detection of Alzheimer's Disease

This project focuses on analyzing MRI data using the OASIS dataset through a hybrid machine learning approach. The model combines convolutional neural networks (CNNs) for processing structural MRI scans with sequential models for analyzing longitudinal health data like clinical scores, cognitive assessments, and demographic information. This dual-stream architecture allows for more comprehensive analysis and potentially earlier detection of Alzheimer's Disease by leveraging both imaging biomarkers and clinical indicators.

## Project Structure

- **data_preprocessing/**
  - `data_preprocessing.ipynb` - Data preprocessing and cleaning
  - `image_separation.ipynb` - MRI image extraction and organization
- **mri_data_analysis/**
  - **data/**
    - `oasis_cleaned.csv` - Processed dataset with clinical variables
  - **trained_models/** - Trained CNN model weights and configurations
  - `mri_data_analysis.ipynb` - CNN model for MRI analysis
- **sequential_data_analysis/**
  - **data/**
    - `oasis_longitudinal_demographics.csv` - Longitudinal patient data
  - `sequential_data_analysis.ipynb` - Sequential data modeling
- `README.md` - Project documentation
- `.gitignore` - Git ignore file

## Setup

### Clone the repository:

   `git clone <repository-url>
   cd <repository-name>`

### Install dependencies

`pip install -r requirements.txt`

## Data

The project uses data from the Open Access Series of Imaging Studies (OASIS) project, specifically OASIS-1 and OASIS-2 datasets. OASIS-1 contains cross-sectional MRI data from 416 subjects aged 18-96, while OASIS-2 provides longitudinal MRI data from 150 subjects aged 60-96, including both normal aging and early-stage Alzheimer's Disease participants. The data has been cleaned and stored in mri_data_analysis/data/oasis_cleaned.csv. Data preprocessing was performed on OASIS-2 data in data_preprocessing.ipynb and on OASIS-3 data in mri_data_separation.ipynb.

Citation: Marcus, D. S., Wang, T. H., Parker, J., Csernansky, J. G., Morris, J. C., & Buckner, R. L. (2007). Open Access Series of Imaging Studies (OASIS): Cross-sectional MRI Data in Young, Middle Aged, Nondemented, and Demented Older Adults. Journal of Cognitive Neuroscience, 19(9), 1498-1507.

## Usage

1. Download OASIS-1 and OASIS-2 datasets and extract them to the `assets` folder:
   ```bash
   # Download and extract OASIS datasets to assets/
   mkdir assets
   ```

2. Preprocess the data:
   ```bash
   # Run Jupyter notebooks for data preprocessing
   data_preprocessing/data_preprocessing.ipynb
   data_preprocessing/image_separation.ipynb
   ```

3. Choose one of the following options:

   A. Train new models:
   ```bash
   # Train CNN model on MRI data
   mri_data_analysis/mri_data_analysis.ipynb
   
   # Train sequential model on longitudinal data
   sequential_data_analysis/sequential_data_analysis.ipynb
   ```

   B. Use pretrained models:
   ```python
   change this
   ```

The pretrained models are optimized for early Alzheimer's detection using the OASIS dataset. For custom applications, training new models is recommended to better fit your specific use case.

## Architecture

The system follows a modular architecture designed for scalability and maintainability. Below is a high-level overview of the system components and their interactions.

[Architecture Diagram - Coming Soon]

### Components

1. **Data Preprocessing Pipeline**
   - Performs data imputation for missing values
   - Segregates and organizes MRI scans into folders
   - Imputes sequential health data
   - Generates cleaned datasets for model training

2. **Model Architecture**
   - CNN model for MRI scan analysis
   - Ensemble model (Naive Bayes + XGBoost) for sequential data
   - Models stored in trained_models directory


3. **Prediction Engine**
   - Combines predictions from both models
   - Predicts Clinical Dementia Rating (CDR) score

4. **Integration Layer**
   - Merges MRI scan analysis with sequential data predictions
   - Generates comprehensive patient assessment
   - Provides final CDR score prediction

The architecture follows a streamlined workflow from data preprocessing to final prediction, combining imaging and sequential data analysis to provide accurate Alzheimer's assessment through CDR scoring.

## Results

Our system demonstrates promising results in early Alzheimer's detection:

[Results coming soon]

- Model performance metrics
- Validation studies
- Comparison with existing methods
- Clinical trial outcomes
- Real-world application results

This section will be updated with detailed performance analysis and validation results.

## Future Prospects

The project has several promising directions for future development and enhancement:
1. **User Interface Development**
   - Web-based dashboard for healthcare providers
   - Mobile application for remote monitoring
   - Intuitive visualization of patient data and predictions

2. **Integration Capabilities**
   - API development for third-party system integration
   - Support for various medical record formats
   - Secure data sharing protocols



These future developments aim to enhance the system's accuracy, usability, and clinical relevance while maintaining its core focus on early Alzheimer's detection.


## Contributing

• Fork the repository

• Create your feature branch:
  ```bash
  git checkout -b feature/amazing-feature
  ```

• Commit your changes:
  ```bash
  git commit -m 'Add some amazing feature'
  ```

• Push to the branch:
  ```bash
  git push origin feature/amazing-feature
  ```

• Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

Rohit Bhandarkar