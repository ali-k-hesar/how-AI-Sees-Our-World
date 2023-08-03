# How AI sees our world

In the quest to understand and interpret the decision-making process of deep learning models, attention maps have emerged as powerful tools. Vision Transformer (ViT) models, which revolutionized computer vision with their attention mechanisms, bring new dimensions to how AI sees and interprets our world. By combining the concepts of Class Activation Map (CAM) and Gradient-weighted Class Activation Map (Grad-CAM) with attention maps from ViT, we gain deeper insights into how these models perceive and analyze images.

## Class Activation Map (CAM):


<div align="center">
  <p>
    <img width="100%" src="https://github.com/ali-k-hesar/how-AI-Sees-Our-World/assets/85279433/88027b27-32e3-48b5-a9d5-1e580a3bc8c5"></a>
  </p>
</div>


CAM is a visualization method to highlight the discriminative regions of an image that contribute the most to a CNN's final classification decision. It works with CNN architectures that employ global average pooling (GAP) layers after the final convolutional layers. CAM calculates the class-specific activations by weighting the feature maps of the last convolutional layer based on their importance in predicting a specific class. This is done by taking a weighted sum of the feature maps, where the weights are determined by the learned weights of the fully connected layer responsible for classification. By overlaying the resulting heatmap on the original image, CAM visually indicates the regions that influenced the network's decision for a particular class.


<div align="center">
  <p>
    <img width="100%" src="https://github.com/ali-k-hesar/how-AI-Sees-Our-World/assets/85279433/8d5d501f-2300-455d-bc76-cb866490b11d"></a>
  </p>
</div>


## Grad-CAM (Gradient-weighted Class Activation Map):


<div align="center">
  <p>
    <img width="100%" src="https://github.com/ali-k-hesar/how-AI-Sees-Our-World/assets/85279433/331407f2-da06-4eff-8d0e-ff4e4c41eef0"></a>
  </p>
</div>


Grad-CAM is an extension of CAM that addresses the limitation of CAM being applicable only to networks with GAP layers. Grad-CAM is more versatile and can be applied to any CNN architecture, even those with multiple fully connected layers. It leverages the gradients flowing into the last convolutional layer to determine the importance of each feature map for a specific class. By computing the gradients of the loss function with respect to the feature maps, Grad-CAM effectively captures the importance of each spatial location in the CNN. Similar to CAM, Grad-CAM produces a heatmap that highlights the regions contributing the most to the classification decision. It provides more fine-grained visualizations, helping researchers and practitioners gain insights into the inner workings of CNNs and the features they use for predictions.


<div align="center">
  <p>
    <img width="100%" src="https://github.com/ali-k-hesar/how-AI-Sees-Our-World/assets/85279433/ec358642-dfee-47f7-a375-4685bde5bc69"></a>
  </p>
</div>


## Attention Map:


<div align="center">
  <p>
    <img width="100%" src="https://github.com/ali-k-hesar/how-AI-Sees-Our-World/assets/85279433/2682f1ed-4c91-4279-a6de-1ad103d90089"></a>
  </p>
</div>


the attention weights of the last layer for the CLS (classification) token in Vision Transformer (ViT) can be used to create an attention map similar to CAM and Grad-CAM in traditional convolutional neural networks (CNNs).

In ViT, the CLS token is a special token appended at the beginning of the input sequence, and it serves as the aggregated representation of the entire image after the self-attention mechanism of the Transformer layers. The attention mechanism in ViT assigns weights to different tokens, including the CLS token, based on their relevance to each other in forming the final representation.

To create an attention map for the CLS token, you can extract the attention weights corresponding to the CLS token from the last self-attention layer of the ViT model. These attention weights represent how much each patch in the input image attends to the CLS token. You can then use these attention weights to weight the embeddings of the patches, similar to CAM and Grad-CAM in CNNs.


<div align="center">
  <p>
    <img width="100%" src="https://github.com/ali-k-hesar/how-AI-Sees-Our-World/assets/85279433/e570be82-8bcc-42ad-a038-bb0514664957"></a>
  </p>
</div>


## Installation

#### 1. Clone the repository:

```shell
git clone https://github.com/ali-k-hesar/how-AI-Sees-Our-World.git
```

#### 2. Install the required dependencies:

```shell
pip install -r requirements.txt
```

#### 3. Run the desired .ipynb file

## License

This project is licensed under the MIT License. See the LICENSE file for details.
