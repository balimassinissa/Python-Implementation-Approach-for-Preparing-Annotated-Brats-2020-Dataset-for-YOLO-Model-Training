# Python-Implementation-Approach-for-Preparing-Annotated-Brats-2020-Dataset-for-YOLO-Model-Training

To execute the code, simply follow these steps:

    # 0-Download the Brats2020 : https://www.kaggle.com/datasets/awsaf49/brats20-dataset-training-validation/data
    # 1-Open a terminal.
    # 2-Type the following command: source myenv/bin/activate
    # 3-Launch Jupyter Notebook by typing: jupyter notebook

You can then run the code.

# Note: You may need to update certain paths for the code to work correctly.
General Informations :
    
    ● Description: Multi-institutional (n=19)
    preoperative MRI Brain scans
    ● File Extension: Neuroimaging Informatics
    Technology Initiative (NIfTI) files (.nii.gz)
    ● Image Size: 240x240x155 Voxels
    ● Number of Training Samples: 369
    Images total
    ● Training Set: 344
    ● Validation and Testing Set: 25 for both


Training:
For training, For training, initially, I used the modalities FLAIR, T1, T1CE, and T2 to create multi-channel images for training. However, I experienced very low precision. For this specific training, I will focus solely on using the T1CE modality. Here’s the process I will follow :

    # 1-Convert to PNG: I convert the T1CE images to PNG format.
    # 2-Resize: I resize the images as needed.
    # 3-Select the Best Slice: I choose the best slice, which is the one containing the most pixels.
    # 4-Start Training: I then proceed to start the training with the selected slice.
    
Results:

                 Class     Images  Instances      Box(P          R      mAP50  m

                   all         14         40      0.664      0.768      0.698      0.352
              Necrosis         13         13      0.384      0.538      0.384      0.123
                 Edema         14         14      0.876      0.929      0.897      0.459
        EnhacingTumors         13         13      0.731      0.836      0.812      0.474

        
![results](https://github.com/user-attachments/assets/feee8c02-14b1-466a-8380-7dadf27df42b)
