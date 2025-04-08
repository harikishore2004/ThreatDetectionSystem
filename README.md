# AI-Powered Cybersecurity Threat Detection System  

The AI-Powered Cybersecurity Threat Detection System is designed to identify and mitigate cyber threats in real-time. By leveraging Machine Learning (ML) and Artificial Intelligence (AI), the system analyzes network traffic, detects anomalies, and predicts potential security threats before they escalate.  

---

## Project Phases  

1️⃣ **Data Collection & Cleaning**  
2️⃣ **AI Model Training**  
3️⃣ **Model Deployment (API Integration)**  
4️⃣ **Real-Time Monitoring Dashboard**  
5️⃣ **Testing & Validation**  

---

## 📌 Phase 1 - Data Collection & Cleaning  

**Clone this repository** 
```sh
git clone https://github.com/harikishore2004/ThreatDetectionSystem.git
cd ThreatDetectionSystem
```
**Create virtual environment**
- For Linux/macOS
```sh
python3 -m venv cybersecenv
source cybersecenv/bin/activate
```
- For Windows
```sh
python3 -m venv cybersecenv
cybersecenv\Scripts\activate
```
**Install the required python libraries**
```sh
pip3 install -r requirements.txt
```
**Connect environment to jupyter notebook**
```sh
python3 -m ipykernel install --user --name cybersecenv
```

### Download the Dataset  
For this project, we are using the **Network Intrusion dataset (CIC-IDS-2017)**.  
You can download it manually from [Kaggle](https://www.kaggle.com/datasets/chethuhn/network-intrusion-dataset).  

Unzip the downloaded file into the **src/rawdata/** folder of the repository.   
The file structure will be: 

```plaintext
.
├── CyberSecurityModel.pkl
├── ModelTraining.ipynb
├── README.md
├── requirements.txt
└── src
    ├── CleanedData.csv
    ├── CombinedDataCleaner.ipynb
    └── rawdata
        ├── Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv
        ├── Friday-WorkingHours-Afternoon-PortScan.pcap_ISCX.csv
        ├── Friday-WorkingHours-Morning.pcap_ISCX.csv
        ├── Monday-WorkingHours.pcap_ISCX.csv
        ├── Thursday-WorkingHours-Afternoon-Infilteration.pcap_ISCX.csv
        ├── Thursday-WorkingHours-Morning-WebAttacks.pcap_ISCX.csv
        ├── Tuesday-WorkingHours.pcap_ISCX.csv
        └── Wednesday-workingHours.pcap_ISCX.csv
```  
  
## Execute the python code
1. **Change to the src Directory**
```sh
cd src/
```
2. **Start jupyter notebook**
```sh
jupyter notebook
```
3. **Open and Run the CombinedDataCleaner Notebook**
Open CombinedDataCleaner.ipynb and execute each cell sequentially.


### Overview of the code
The program performs the following tasks:  
- **Feature Selection:** Selecting the most relevant attributes from the dataset that are best suited for our specific use case.
- **Data Cleaning:** Removing rows containing NaN (Not a Number) values and duplicates to reduce errors.
- **Normalizing Values:** Scaling large values down to a smaller range to improve model performance during training.

## 📌 Phase 2 - AI Model Training  

In this phase, we train our Machine Learning model to classify network traffic and identify potential cyber threats.  
We use the `Random Forest Classifier` due to its robustness and effectiveness in handling complex datasets with high dimensionality.

### Steps to Train the Model:

1. **Start Jupyter Notebook**  
   ```sh  
   jupyter notebook  
   ```
2. **Open and Run the Training Notebook**
Open `ModelTraining.ipynb` and execute each cell sequentially.

### What are the steps included in this phase:

* **Data Loading:** The cleaned and preprocessed dataset is loaded.

* **Train-Test Split:** The data is divided into training and testing sets to train and evaluate model accuracy.

* **Model Training:** A Random Forest Classifier is trained to recognize patterns in malicious vs. benign traffic.

* **Evaluation:** Model performance is assessed using by calculating the accuracy of the model.

* **Model Export:** The trained model is saved as CyberSecurityModel.pkl for later use in the deployment phase.

