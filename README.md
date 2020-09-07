# Code_JFSE
This is the source code of "Joint Feature Synthesis and Embedding: Adversarial Cross-modal Retrieval Revisited".
## Introduction
This is the JFSE, the Tensorflow source code for the paper "Joint Feature Synthesis and Embedding: Adversarial Cross-modal Retrieval Revisited" from UESTC. 
<br>
<br>

   ![framework](https://github.com/CFM-MSG/Code_JFSE/fig/flowchart.png)

<br>

### What task does our code (method) solve?
JFSE propose an advanced network architecture of coupled conditional WGANs to synthesize multimodal data in the semantic feature space to complement the true data to overcome the lack of labeled cross-modal data in the available multimodal datasets. Unlike most existing studies only focus on the standard cross-modal retrieval scenario, JFSE further explore the more practical scenarios of zero-shot and generalized zero-shot cross-modal retrieval scenarios. 

### Insight of our model:
- Effective cross-modal feature synthesis with improved GAN structure to produce meaningful synthetic features and to learn more effective common embedding space.
- Advanced common embedding space learning. To support both standard retrieval, zero-shot and generalized Zero-shot retrieval tasks, we develop three advanced distribution alignment schemes to capture cross-modal correlation and enable the knowledge transfer during common embedding space learning. Besides, to enable the knowledge transfer between classes, we introduce an advanced cycle-consistency constraint that preserves the semantic compatibility between original features and the mapped common features of both true and synthetic data.

### The State-of-the-art Performance 
#### Standard retrieval
<br>

 <img src="https://github.com/CFM-MSG/Code_JFSE/fig/standard.png" width="90%" />
 
#### Zero-shot retrieval
<br>

 <img src="https://github.com/CFM-MSG/Code_JFSE/fig/zsl.png" width="90%" />
 
 #### Generalized zero-shot retrieval
<br>

 <img src="https://github.com/CFM-MSG/Code_JFSE/fig/gzsl.png" width="90%" />

More details can be referred to our paper

## Installation and Requirements
### Installation
We recommended the following dependencies:
- Python 3
- Tensorflow > 1.0
- Numpy
- pickle
  
## Training
### Data Download
Data Preparation: We use [PKU XMediaNet dataset](http://59.108.48.34/tiki/XMediaNet/) as example, and the data should be put in ./data/. The data files can be download from the [link](http://59.108.48.34/mipl/tiki-download_file.php?fileId=1012) and unzipped to the above path.

### Running
Run demo.py to train models and calculate mAP
```
python demo.py
```

```
