# Exploring-Deep-Learning-Models-for-Polyp-Segmentation-on-Kvasir-SEG-Dataset-a-Comparative-Analysis

# Data Source:
The research uses the Kvasir-SEG dataset, an open-access collection containing 1000 gastrointestinal polyp images with corresponding segmentation masks. The images vary in resolution from 332x487 to 1920x1072 pixels and present challenges such as heterogeneous shapes, lighting variations, and artifacts like motion blur.

# Workflow:
## Data Preprocessing:

The dataset was split into 80% training, 10% validation, and 10% testing sets.
Data augmentation techniques included rescaling, flipping, rotation, zoom, and brightness adjustments to enhance the model's resilience and performance. All images were resized to 256x256 pixels and normalized to a range of 0 to 1.
## Model Selection:

Five deep learning models were explored: FCN8, FCN16, FCN32, PEFNet, and DeepLabV3+.
Transfer learning was employed using pre-trained models (VGG19, VGG16, ConvNextSmall, and ResNet50) from the ImageNet dataset. The models were compiled with the Adam or AdamW optimizers and trained for 80 epochs.
## Metrics:

The performance was evaluated using accuracy, Dice Similarity Coefficient (DSC), and Intersection over Union (IoU).
# Results:
PEFNet achieved the highest performance with 96.07% accuracy, 89.71% DSC, and 81.70% IoU, indicating superior segmentation performance.
DeepLabV3+ followed with 94.43% accuracy, 84.90% DSC, and 74.17% IoU.
FCN32 reached 92.06% accuracy, but its DSC and IoU were lower compared to PEFNet and DeepLabV3+.
FCN16 and FCN8 showed the lowest performance, with accuracies of 84.60% and 83.46%, respectively, and lower DSC and IoU scores.

# Conclusion:
The study demonstrates that PEFNet and DeepLabV3+ are highly effective for polyp segmentation tasks on the Kvasir-SEG dataset, outperforming traditional models like FCN. Further improvements could be made by addressing potential overfitting and fine-tuning hyperparameters
