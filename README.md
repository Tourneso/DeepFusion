## This is the online repository of the paper titled "DeepFusion: Smart contract vulnerability detection via deep learning and data fusion".

DeepFusion is an Ethereum smart contract vulnerability detection method, it can detect 5 types of Solidity smart contract vulnerabilities.


## Task Definition

Detect reentrancy, timestamp dependence, integer overflow and underflow, Use tx.origin for authentication and Unprotected Selfdestruct Instruction vulnerabilities in smart contract.

## Requirements

#### Required Packages
* **python**3
* **TensorFlow**1.14.0 
* **keras** with TensorFlow backend
* **sklearn** for model evaluation

Run the following script to install the required packages.
```shell
pip install --upgrade pip
pip install tensorflow==1.14.0
pip install keras
pip install scikit-learn
```

## Structure in this project

```
${DeepFusion}
├── dataset
│   ├── IntergerOverOrUnderFlow
│   │   └── ast.txt
│   │   └── code_slicing.txt
│   ├── reentrancy
│   │   └── ast.txt
│   │   └── code_slicing.txt
│   └── Selfdestruct
│   |   └── ast.txt
│   |   └── code_slicing.txt
│   └── timestamp
│   |   └── ast.txt
│   |   └── code_slicing.txt
│   └── txOrigin
│   |   └── ast.txt
│   |   └── code_slicing.txt
├── models
    ├── representation_fu_BLSTM_Attention.py
├── ProgmaSlicing
    ├── ree
    │   └── sourceCode
    │   └── main.py
    │   └── progmaSlicing_code.py
```

- `dataset`: This is results of two kinds of data processing.
- `models/representation_fu_BLSTM_Attention.py`: This is the training and testing model of fused data.
- `ProgmaSlicing/ree/progmaSlicing_code.py`: This is to extract code slicing information of re-entrancy vulnerability.
