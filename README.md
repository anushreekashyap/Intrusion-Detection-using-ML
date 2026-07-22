# Intrusion Detection using ML

## Overview

The **Intrusion Detection System (IDS)** is a Python-based cybersecurity project that simulates network traffic and identifies potential intrusions using simple rule-based detection. The system generates random network traffic records, analyzes selected network parameters, and classifies each record as either **Normal** or **Attack** based on predefined conditions.

This project demonstrates the fundamental concepts of intrusion detection, network traffic analysis, and cybersecurity using a command-line interface.

---

## Features

- Generates random network traffic data.
- Simulates network parameters such as:
  - Duration
  - Source Bytes
  - Destination Bytes
- Detects suspicious network activity using predefined rules.
- Allows users to test custom network traffic.
- Displays detection results instantly.
- Simple and beginner-friendly Python implementation.

---

## Technologies Used

- Python 3.x
- Random Module (Built-in)

---

## Detection Logic

The system classifies network traffic using the following rules:

- **Attack**
  - Duration > 900
  - OR Source Bytes > 8000

- **Normal**
  - All other network traffic

---

## Project Structure

```
Intrusion-Detection-using-ML/
│
├── intrusion_detection.py
├── README.md

```

---

## How to Run

### Clone the Repository

```bash
git clone https://github.com/yourusername/Intrusion-Detection-using-ML.git
```

### Navigate to the Project Folder

```bash
cd Intrusion-Detection-using-ML
```

### Run the Program

```bash
python intrusion_detection.py
```

---

## Sample Output

```
========================================
      INTRUSION DETECTION SYSTEM
========================================

Generated Network Traffic:

1. Duration: 245 | Src Bytes: 3200 | Dst Bytes: 4100 | Status: Normal
2. Duration: 956 | Src Bytes: 8700 | Dst Bytes: 2100 | Status: Attack
...
20. Duration: 187 | Src Bytes: 4500 | Dst Bytes: 6200 | Status: Normal

========================================
      TEST CUSTOM NETWORK TRAFFIC
========================================

Enter Duration: 950
Enter Source Bytes: 6000
Enter Destination Bytes: 2000

Result: ATTACK DETECTED

System Finished Successfully
```

---

## Future Enhancements

- Use real intrusion detection datasets (NSL-KDD, CICIDS2017, UNSW-NB15).
- Integrate Machine Learning algorithms.
- Add graphical data visualization.
- Develop a web-based dashboard.
- Improve attack classification accuracy.

---

## Author

**Anushree Kashyap**

Bachelor of Computer Applications (BCA)

Cybersecurity Enthusiast
