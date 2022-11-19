### Character recognition and Image segmentation

The main goal of the project is to recognize the character in a set of images. The characters are from 0 to 9 and from a to z. 

#### Dataset :

For the training dataset, we have two images per row. A noisy image and its corresponding mask. 
For the test dataset, we just have the noisy image.

#### Approach :

For the classification task, it will be easier to give our model images without noise as input. To do so, we first use a U-NET architecture for semantic segmentation [https://arxiv.org/pdf/1505.04597v1.pdf] in order to generate the masks of the test dataset. 
Once we have generated the masks of the test set, we will build a CNN model for character recognition based on the masks.