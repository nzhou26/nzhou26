# Interview Preparation Questions

## Deep Learning and Machine Learning

### Model Architecture and Design
- Explain the architecture of EfficientNet, U-Net, YOLO, Mask R-CNN, ViT, and CLIP.
    * The key of EfficientNet is compound scaling, meaning increasing the dimension of its network without lossing accuracy. 
    * U-net is mainly used for semantic segmentation. The key aspect of U-net is encoder, upsamling, and skip connection
    * Mask R-CNN contains key component of ROIAlign and Feature Pyramid Network. ROIAlign consists of Bilinear Interpolation ( For each bin, ROI Align computes the exact values using bilinear interpolation from the **nearest four points** on the feature map. This avoids any rounding and keeps the spatial information intact.). FPN using features from different scales
    * ViT doesn't use CNN, it splits image to **patches**, and flatten every patch. Positional encoder to retain spatial information and transformer encoder consists of MLP. 
    * CLIP consists two parts, one image encoder and one text encoder, these features then projected into shared embedding space
- How would you choose an appropriate model for a given task?
    * Mainly depend on which its a classification or segmentation or object detection
- Discuss the trade-offs between different model architectures.
    * Speed is not a limitation as far as we concern, so accuracy is more important, unless there's a requirement for instant response. In that case, yolo will be used. 
### Training and Optimization
- How do you handle overfitting and underfitting in your models?
    * Most of overfitting are solved by adding more dataset
    * Underfitting means we might want to change model
- Explain different optimization techniques (e.g., Adam, SGD) and regularization methods (e.g., dropout, weight decay).
    * SGD optimizes incrementally by batch, and learning rate is fixed so it can be noisy
    * Adam is more adaptive and uses momentum
- Describe the process of fine-tuning a pre-trained model.
    * checking data
    * augmentation
    * train-val-test split
    * training model
    * validation
    * run on test mode and ensure metrics, and always test on the same test set to make models comparable

### Data Handling and Preprocessing
- How do you handle imbalanced datasets?
    * merge label
    * data augmentation
    * remove duplicates data from larger class
- Describe your approach to data augmentation.
    * slicing, zoom-in, cropping, rotate, adjust brightness, mainly to mimick real case scenario
- Explain the importance of data normalization and how you perform it.
    * I most do a 255 division, which is a normalization for image
    * But when I'm comparing two cross-correlation features. I need to know which peak is sharper. I will to a standardization 
### Evaluation Metrics
- What metrics do you use to evaluate the performance of a model?
    * mAP 75, precision, recall, F1 score
- How do you interpret the confusion matrix, precision, recall, F1 score, and mAP (mean Average Precision)?
    * confusion matrix tells us which two or more classes are harder to separated by model, so we have to check images to see their similarity or difference. Precision means the ratio the class we pred are corrected devided by the total predications. Recall mean how many case of ground truth there we are able to recover. F1 is a overall indicator to ensure our model performance. 

## Computer Vision

### Image Segmentation and Object Detection
- Explain how YOLO and Mask R-CNN work for object detection and segmentation.
- Discuss the challenges you faced in semantic segmentation and how you addressed them.
    * Most of the time we faced data imbalance and inaccuracy. We have to visualize our data and balance our data
### Image Processing Techniques
- Describe various image processing techniques you have used (e.g., filtering, edge detection, morphological operations).
- How do you perform image registration and alignment?

## Bioinformatics and Cryo-EM

### Bioinformatics Algorithms
- Discuss the algorithms and tools you used for bioinformatics projects.
- How do you handle large-scale genomic data?

### Cryo-EM Data Processing
- Explain the steps involved in preprocessing and data collection for Cryo-EM.
- How does semantic segmentation improve atomic reconstruction in Cryo-EM?

## Software Development and Deployment

### Programming Languages and Tools
- Discuss your experience with Python, Bash, and Node.js.
- How do you use Docker for containerization and deployment?

### API and Microservices
- Explain how you design and implement RESTful APIs.
- Discuss your experience with RabbitMQ, Redis, and SQL.

### Version Control and Collaboration
- Describe your workflow with Git for version control.
- How do you handle collaboration and code reviews in a team setting?

## System Design and Architecture

### System Decoupling
- Explain the process of decoupling a monolithic system into microservices.
- Discuss the advantages and challenges of using a microservices architecture.

### Real-Time Systems
- How do you ensure real-time processing and analysis of data?
- Describe your approach to handling high-throughput data streams.

## Innovation and Future Directions

### Emerging Technologies
- How do you stay updated with the latest advancements in deep learning and computer vision?
- Discuss any innovative projects you are currently working on or planning to start.

### Integration of AI and NLP
- How can NLP be integrated with computer vision models for industrial automation?
- Describe the potential benefits and challenges of multi-model AI systems.

## Publications and Research

### Research Contributions
- Discuss the key findings and contributions of your publications.
- Explain the significance of your research in the broader scientific context.
