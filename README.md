# AI-Powered Cybersecurity Threat Detection System  

The **AI-Powered Cybersecurity Threat Detection System** is designed to **identify and mitigate cyber threats in real-time**. By leveraging **Machine Learning (ML) and Artificial Intelligence (AI)**, the system analyzes network traffic, detects anomalies, and predicts potential security threats before they escalate.  

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
python3 -m venv myenv
source myenv/bin/activate
```
- For Windows
```sh
python3 -m venv myenv
myenv\Scripts\activate
```
**Install the required python libraries**
```sh
pip3 install -r requirements.txt
```
**Connect environment to jupyter notebook**
```sh
python3 -m ipykernel install --user --name myenv
```

### Download the Dataset  
For this project, we are using the **Network Intrusion dataset (CIC-IDS-2017)**.  
You can download it manually from [Kaggle](https://www.kaggle.com/datasets/chethuhn/network-intrusion-dataset).  

Unzip the downloaded file into the **rawdata/** folder of the repository.  

```plaintext
├── README.md
├── requirements.txt
└── src
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
Change to the src Directory
```sh
cd src/
```
Start jupyter notebook 
```sh
jupyter notebook
```
Open CombinedDataCleaner.ipynb and execute the cells.  

### Overview of the code
The program performs the following tasks:  
- **Feature Selection:** Selecting the most relevant attributes from the dataset that are best suited for our specific use case.
- **Data Cleaning:** Removing rows containing NaN (Not a Number) values and duplicates to reduce errors.
- **Normalizing Values:** Scaling large values down to a smaller range to improve model performance during training.
