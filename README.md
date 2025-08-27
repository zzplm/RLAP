## Reproducibility Statement

### Code Availability
&nbsp;&nbsp;&nbsp;&nbsp;All code is provided in **Jupyter notebook format** within this repository.The notebooks include detailed annotations, enabling readers to follow the implementation easily.We have also added an extended **README** file that offers further explanations and experiment-specific details.

### Experimental Setup
&nbsp;&nbsp;&nbsp;&nbsp;We provide three independent experiments based on different datasets: **MNIST**, **CIFAR-10**, and **Speech Commands**.While the overall methodology is consistent with *Figure 1 (page 8)* of the paper, the training and attack configurations differ across datasets due to variations in dataset size and characteristics.  

- **MNIST**: lightweight experiment for quick validation.  
- **CIFAR-10** and **Speech Commands**: main experiments reported in the manuscript, demonstrating the effectiveness of our method.  

All experiments were run on **NVIDIA GPUs**. Please ensure that **CUDA**, **PyTorch**, and **TensorFlow** are properly configured prior to running the experiments.  

### Dataset-Specific Instructions

#### MNIST
- **Purpose**: Quick validation and testing of extensions.  
- **Implementation**:  
  - Initial notebook cells handle preprocessing and base network training.  
  - Multiple variables are available and can be adjusted through annotations.  
  - **Data partitioning**: GMM was used in our final setup, but alternative methods are also included.  
  - **Reports**: intermediate results are printed during execution.  
  - **Neural pruning**: pruning ratios and parameters are adjustable. Additional commented code for multi-layer extensions is provided.  
  - **Fine-tuning**: two sets of parameter options are available depending on runtime.  

#### CIFAR-10
- **Purpose**: Main experiment presented in the manuscript.  
- **Implementation**:  
  - Same structure as MNIST.  
  - **Table 1 (p.16), Table 3 (p.17), Table 4 (p.18), and Table 5 (p.19)** can be reproduced by modifying parameters in the first notebook section.  
  - **Table 2 (p.16)** requires running additional comparative experiments (files included in the repo).  
  - Includes an additional **retraining module** not present in MNIST.  
  - Each notebook cell prints progress updates and intermediate results.  

#### Speech Commands
- **Purpose**: Validation in speech processing scenario.  
- **Implementation**:  
  - Requires **TensorFlow**.  
  - Workflow: preprocessing and training → data partitioning → pruning and fine-tuning → retraining.  
  - Code is concise: modifying the first section is sufficient to reproduce **Table 6 (p.22)**.  

### Summary
&nbsp;&nbsp;&nbsp;&nbsp;By combining the Jupyter notebooks, annotations, and the extended README file, researchers should be able to reproduce the reported experimental results with minimal effort.The repository is designed to allow straightforward extension and modification for new experimental settings.  
