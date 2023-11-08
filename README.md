# SimCLR
SimCLR is a self-supervised learning strategy.
The most promising use of the SimCLR model is to train your encoder model(e.g. Resnet18) and then perform the downstream task on the model such as classification or regression.
The SimCLR framework has four major components:
1. A DataAgumentation module that is explained in this paper https://arxiv.org/pdf/2002.05709.pdf.
2. A basic encoder like resnet18.
3. A Projection head that maps the data to where the constrastive loss is to be applied.
4. which is low if the two correlated vectors generated from the data augmentation module (from the same original image) are similar to each other AND dissimilar to the vectors from all the “negative” examples of the other images and high otherwise.
