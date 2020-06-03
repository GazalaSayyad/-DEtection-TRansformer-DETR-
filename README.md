# -DEtection-TRansformer-DETR-
Facebook AI Launches DEtection TRansformer (DETR) – A Transformer based Object Detection Approach!
Introduction:
This new model is quite simple and you don’t have to install any library to use it. DETR treats an object detection problem as a direct set prediction problem with the help of an encoder-decoder architecture based on transformers. By set, I mean the set of bounding boxes. Transformers are the new breed of deep learning models that have performed outstandingly in the NLP domain.

Architecture of DETR:
The overall DETR architecture is actually pretty easy to understand. It contains three main components:

1.a CNN backbone
2.an Encoder-Decoder transformer
3.a simple feed-forward network



Here, the CNN backbone generates a feature map from the input image. Then the output of the CNN backbone is converted into a one-dimensional feature map that is passed to the Transformer encoder as input. The output of this encoder are N number of fixed length embeddings (vectors), where N is the number of objects in the image assumed by the model.

The Transformer decoder decodes these embeddings into bounding box coordinates with the help of self and encoder-decoder attention mechanism.

Finally, the feed-forward neural networks predict the normalized center coordinates, height, and width of the bounding boxes and the linear layer predicts the class label using a softmax function.
