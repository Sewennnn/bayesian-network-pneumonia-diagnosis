🧠 Bayesian Network for Pneumonia Diagnosis
 
📌 Overview
This project models a medical diagnosis system using:

- Bayesian Networks (BN)
- Bayesian Decision Networks (BDN)

The system estimates the probability of bacterial, viral, or no pneumonia based on patient features such as:

- Age
- Symptoms (fever, breathing, lung sounds)
- Vaccination status
- X-ray results

It further extends into a decision-making model to determine:

- Whether to perform an X-ray
- Whether to administer antibiotics

  
🎯 Objectives

- Model uncertainty in medical diagnosis using probabilistic reasoning
- Combine expert knowledge and literature data
- Perform inference under incomplete information
- Optimize decisions using expected utility theory


🧠 Key Concepts

🔷 Bayesian Network (BN)
- Directed acyclic graph (DAG)
- Nodes represent variables (e.g. Pneumonia type, Fever)
- Edges represent probabilistic dependencies
- CPTs (Conditional Probability Tables) define relationships

  
🔷 Bayesian Decision Network (BDN)
Extends BN with:
- Decision nodes
- Utility nodes
- Enables optimal decision-making under uncertainty

  
🏗️ Model Structure

Nodes include:
- Pneumonia Type (Bacterial / Viral / None)
- Age group
- Fever
- Rapid breathing
- Lung crackling
- X-ray result
- Vaccination status
  
Extensions (BDN):
- Decision: Perform X-ray
- Decision: Give antibiotics
  
Utilities:
- Cost of X-ray
- Cost of treatment
- Health outcomes

  
📊 Data Sources

Model parameters are derived from:

- 🧑‍⚕️ Medical Expert (ME) knowledge
- 📚 Literature studies (LIT)
- ⚠️ Some reasonable assumptions where data was incomplete

🔍 Inference & Analysis

The model supports:

- Prior probability estimation
- Posterior inference given symptoms
- Comparative diagnosis between patients
- Sensitivity analysis on parameters
- Evaluation of diagnostic tests (TPR, FPR)


⚖️ Decision-Making (BDN)

The system computes Expected Utility (EU) to determine:

Whether an X-ray should be performed
Whether antibiotics should be administered

Decisions balance:

- Risk of untreated bacterial pneumonia
- Cost/harm of unnecessary treatment
- Diagnostic accuracy of tests


📁 Project Files
```
bayesian-network-pneumonia-diagnosis/
│
├── README.md
├── report/
│   └── diagnosis_report.pdf
│
├── models/
│   ├── bn_structure.dne       
│   ├── bn_parameterized.dne   
│   ├── bdn_extended.dne        
│
├── screenshots/
│   ├── bn_structure.png
│   ├── parameterized_network.png
│   ├── decision_network.png

```



🚀 Key Learnings
  
- Probabilistic reasoning in real-world systems
- Building and parameterizing Bayesian Networks
- Decision-making under uncertainty
- Sensitivity analysis of probabilistic models
- Combining multiple knowledge sources (expert + data)

  
💡 Possible Extensions

- Learn CPTs from real-world datasets instead of manual estimation
- Integrate with Python libraries (e.g. PyMC, pgmpy)
- Expand model with more clinical variables
- Deploy as an interactive diagnostic tool
