# CMFF6D
Cross-modality Multiscale Feature Fusion Network for 6D Pose Estimation
## Installation - From conda
-   Install conda environment from conda environment.yml (it might take a while, and don't forget changing the prefix in the end of environment.yml file)
```bash 
conda env create -f cmff6d/environment.yml
```
- Activate our cmff6dtest conda environment
```bash
conda activate cmff6dtest
```
- Install mmseg within conda
```bash 
pip install -r cmff6d/mmseg_install.txt
```
- Following [normalSpeed](https://github.com/hfutcgncas/normalSpeed) to install normalSpeed within conda
```bash
pip3 install "pybind11[global]"
git clone https://github.com/hfutcgncas/normalSpeed.git
cd normalSpeed
python3 setup.py install --user
```
- Install some neccessary package
```bash 
cd models/RandLA
sh compile_op.sh
```  
## Code Structure

## Datasets
- ### Download real and prepare synthetic LineMod Dataset 
  - Download the preprocessed LineMOD dataset from [onedrive link](https://hkustconnect-my.sharepoint.com/:u:/g/personal/yhebk_connect_ust_hk/ETW6iYHDbo1OsIbNJbyNBkABF7uJsuerB6c0pAiiIv6AHw?e=eXM1UE) or [google drive link](https://drive.google.com/drive/folders/19ivHpaKm9dOrr12fzC8IDFczWRPFxho7) (refer from [DenseFusion](https://github.com/j96w/DenseFusion)). Unzip it and link the unzipped ``Linemod_preprocessed/`` to ``ffb6d/datasets/linemod/Linemod_preprocessed``:
  ```shell
  ln -s path_to_unzipped_Linemod_preprocessed ffb6d/dataset/linemod/
  ```
- ### Download MP6D Dataset
链接：https://pan.baidu.com/s/1FX9OdbaVrUT1d6W6dkcmUA 
提取码：by9r
## Training and evaluating
### Training on the LineMOD Dataset

- Train the model for the target object.
      ``` bash sh train_lm.sh ```

### Evaluating on the LineMOD Dataset

- Start evaluation by:
      ``` bash sh test_lm.sh ```
`
### Evaluating on the Occ-LineMOD Dataset

- Start evaluation by:
      ``` bash sh test_occlm.sh ```

### Training on the MP6D Dataset

- Train the model for the target object. 
  
  ``` bash sh train_meta.sh ```

### Evaluating on the MP6D Dataset

- Start evaluation by:
      ``` bash sh test_meta.sh ```
