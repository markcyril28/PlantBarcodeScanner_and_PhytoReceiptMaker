
# PlantBarcodeScanner_and_PhytoReceiptMaker

Post-processing pipeline for plant barcoding genes such as *ITS*, *matK*, and *rbcL*.

---

## A. Preparation of the Environment and Dependencies.
### 1. Activate your WSL

- Tutorial: [How to Install WSL](https://www.youtube.com/watch?v=5RTSlby-l9w)  
  **Note:** Install **Ubuntu 22** instead of the version shown.

### 2. Downloading and Initializing Conda

Reference: [Installing Miniconda on Linux](https://www.anaconda.com/docs/getting-started/miniconda/install#linux-terminal-installer)

```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
source ~/.bashrc
````

### 3. Creating a Conda Environment: Basic Cheatsheet

```bash
conda create -n PlantBarcodeScanner_env
conda activate PlantBarcodeScanner_env
conda deactivate
```

---

## B. Preparation of Softwares and Website to be used. 

### UniPro Gene for viewing and 01_Quality_Control of the sequences.
1. Download UniPro UGENE from their [official websites](https://ugene.net/download-all.html). 
2. Install the UniPro UGENE. 
3. View the ab1 file in the UniPro UGENE software. 

### MEGA Command Line Version for 05_Phylogenetic_Analysis. 
1. Download **megacc** (MEGA Command-line version) from their [official website](https://www.megasoftware.net/):

   * Choose **Ubuntu/Debian**, **Command Line (CC)**, and version **MEGA 11**.
   * Place the downloaded `.deb` file in your working directory.
   * Install using:

```bash
sudo dpkg -i mega_11.0.13-1_amd64.deb
```

### Clustal Omega for 04_Multiple_Sequence_Alignment.

#### Command-line version 
1. Open WSL. Activate your conda environment for your analysis.  
2. Install Clustal Omega (clustalo) from conda using the script below while inside the conda environment.

```bash
conda install clustalo
```
#### Website version. 
1. Go to their [website](https://www.ebi.ac.uk/jdispatcher/msa/clustalo). 
2. Input your sequence. 
3. Wait for the result. 