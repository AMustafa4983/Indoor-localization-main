# Indoor Localization System

## Overview
The Indoor Localization System is a machine learning-based solution for indoor positioning and navigation. It uses Wi-Fi fingerprinting techniques to determine the location within a building. The system is designed to be robust and accurate, leveraging deep learning models for building and floor classification, as well as coordinate regression.

## Features
- **Wi-Fi Fingerprinting**: Utilizes Wi-Fi signal strength data for indoor positioning.
- **Building and Floor Classification**: Deep learning models to classify the building and floor based on Wi-Fi signals.
- **Coordinate Regression**: Predicts precise coordinates within a building.
- **Data Preprocessing**: Includes scripts for cleaning and preparing the dataset for training.
- **Visualization**: Notebook for visualizing signal data and model predictions.

## Dataset
The dataset includes Wi-Fi signal strength readings (`Training_rss_21Aug17.csv`, `Test_rss_21Aug17.csv`), coordinates (`Training_coordinates_21Aug17.csv`, `Test_coordinates_21Aug17.csv`), and access point positions (`AP_postions.csv`). 

## Models
- **Building Classifier (`Building_classifier.h5`)**: Classifies the building based on Wi-Fi signals.
- **Floor Classifier (`Floor_classifier.h5`)**: Determines the floor within the building.
- **Regressor (`Regressor.h5`)**: Predicts the x, y coordinates within the building.

## Installation and Usage

1. **Clone the Repository**
   ```
   git clone https://github.com/AMustafa4983/Indoor-localization-main.git
   cd Indoor-localization-main
   ```

2. **Install Dependencies**
   ```
   pip install -r requirements.txt
   ```

3. **Run the Jupyter Notebook**
   ```
   jupyter notebook notebook/indoor-locallization.ipynb
   ```

## Contributing

Contributions to improve the system's accuracy or extend its capabilities are welcome. Please follow the standard fork-and-pull request workflow for contributions.

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## License

This project is open-sourced under the MIT License. See the [LICENSE](LICENSE) file for more details.
