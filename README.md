# Google-Colab-9
Using VGGFace for face verification.
The steps are as follows.

- Upload dataset of images to workbook.
- Pip install VGGFace and MTCNN.
- Load various libraries.
- Read folder names as labels and append to label list.
- Load VGGFace with senet50 with include_top as false to be able to extract embeddings.
- Iteratively find the embeddings of all images in the dataset and add to the embedding list.
- Identify one person in the dataset as a test case and load new photo for him which the model has not seen before.
- Run the new photo of test case through the model and obtain embedding.
- Iteratively check the Cosine distance between the embedding of the test photo and embedding of all the images in the dataset.
- Declare a match in the case where the model finds a Cosine distance of less than 0.4
