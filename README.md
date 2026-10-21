# IoT Sensor Anomaly Detection Using Machine Learning

## Overview
This project demonstrates unsupervised anomaly detection using the Isolation Forest algorithm on simulated industrial sensor data. It analyses temperature and vibration readings to identify unusual patterns that could indicate potential equipment issues.

## Objectives
- Generate simulated normal sensor readings and artificial anomalies.
- Apply Isolation Forest to identify unusual readings.
- Evaluate predictions using a confusion matrix, precision, recall, and accuracy.
- Compare contamination settings and their effect on false alarms.

## Technologies
- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Methodology
1. Generate 1,000 simulated normal sensor readings.
2. Create 30 artificial anomalies with elevated temperature and vibration values.
3. Train an Isolation Forest model using normal readings only.
4. Evaluate the model on the combined dataset.
5. Compare contamination settings of 0.03 and 0.01.

## Results

| Metric | Contamination 0.03 | Contamination 0.01 |
|---|---:|---:|
| False alarms | 30 | 10 |
| Artificial anomalies detected | 30/30 | 30/30 |
| Anomaly precision | 50% | 75% |
| Anomaly recall | 100% | 100% |
| Accuracy | 97.09% | 99.03% |

Reducing contamination from 0.03 to 0.01 reduced false alarms by approximately 66.7% while retaining 100% recall on this test dataset.

## Limitations
The dataset is simulated, and the artificial anomalies are clearly separated from most normal readings. The experiment is a proof of concept, not a validated industrial monitoring system. The evaluation uses the same simulated normal observations for training and testing, so further testing on independent data is needed.

## Future Improvements
- Evaluate the model on a separate, independently generated test dataset.
- Test more subtle and realistic anomalies.
- Explore additional anomaly-detection algorithms.
- Investigate real industrial sensor datasets.

## Notebook
See the Jupyter Notebook in this repository for the implementation, visualisations, and evaluation.

**Disclaimer:** All sensor readings in this project are simulated; no real industrial equipment was monitored.
