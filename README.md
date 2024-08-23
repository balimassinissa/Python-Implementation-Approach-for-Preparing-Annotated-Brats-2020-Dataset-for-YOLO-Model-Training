# Python-Implementation-Approach-for-Preparing-Annotated-Brats-2020-Dataset-for-YOLO-Model-Training

To execute the code, simply follow these steps:

    # 0-Download the Brats2020 : https://www.kaggle.com/datasets/awsaf49/brats20-dataset-training-validation/data
    # 1-Open a terminal.
    # 2-Type the following commands : 
                                        1 python3 -m venv myenv    
                                        2 source myenv/bin/activate
                                        3 pip install nibabel matplotlib
                                        4 pip install SimpleITK matplotlib
                                        
    # 3-Launch Jupyter Notebook by typing: jupyter notebook

You can then run the code.

### Important Note: You may need to update certain paths for the code to work correctly.
General Informations :
    
    ● Description: Multi-institutional (n=19)
    preoperative MRI Brain scans
    ● File Extension: Neuroimaging Informatics
    Technology Initiative (NIfTI) files (.nii)
    ● Image Size: 240x240x155 Voxels
    ● Number of Training Samples: 369
    Images total
    ● Training Set: 344
    ● Validation and Testing Set: 25 for both


Training:
For training, initially, I used the modalities FLAIR, T1, T1CE, and T2 to create multi-channel images for training. However, I experienced very low precision. For this specific training, I will focus solely on using the T1CE modality. Here’s the process I will follow :

    # 1-Convert to PNG: I convert the T1CE images to PNG format.
    # 2-Resize: I resize the images as needed.
    # 3-Select the Best Slice: I choose the best slice, which is the one containing the most pixels.
    # 4-Start Training: I then proceed to start the training with the selected slice.

Results Training :
![results](https://github.com/user-attachments/assets/c06c2041-441b-4096-ac58-a05c7ad1fb3b)


Results Val:

                Class     Images  Instances      Box(P          R      mAP50  m

                   all         14         40      0.735      0.693      0.734      0.375
              Necrosis         13         13      0.471      0.385      0.421      0.114
                 Edema         14         14      0.826      0.929      0.928      0.529
       EnhancingTumors         13         13      0.909      0.765      0.853      0.482

        


