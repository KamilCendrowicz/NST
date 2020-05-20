
## What is NST?

Neural style transfer is an optimization technique that uses a pretrained CNN called VGG19. It is used used to take two images, a content image, a style reference image and combine them together in order to create a version of your image painted by your favourite painter.

The network is able to decect important details in the content image and keep then untouched. While the important parts are stylized as little as they can in order for them to be recognizable the rest of the image is stylized heavily.

## What is VGG19?

VGG19 is a Convolutional Neural Network (CNN) that is key to NST. It consists of 1,000 classes, training set of 1.2 million images, a validation set of 50 thousand images and a test set of 150 thousand images. 

In order to classify layers of the contsent image and distinguish the most important elements a versitile model such as VGG is needed.

## Steps

 1. Visualize the input
 2. Define content and style
 3. Build the model
 4. Calculate style
 5. Extract style and content
 6. Use gradient descent
 7. Run variation loss
 8. Re-run optimazation

For more detailed information feel free to look into out notebook.

## Academic papers

For more detailed and technical information on NST we recommend this paper:
https://arxiv.org/pdf/1508.06576.pdf

# Project was based on:

Theoretical knowledge from: [TowardsDataScience](https://towardsdatascience.com/light-on-math-machine-learning-intuitive-guide-to-neural-style-transfer-ef88e46697ee)

More insight on loss function: [Medium Article](https://medium.com/tensorflow/neural-style-transfer-creating-art-with-deep-learning-using-tf-keras-and-eager-execution-7d541ac31398)

Algorithm of artistic style: [Cornell University](https://arxiv.org/abs/1508.06576)

Gradient Descent: [ML Course](https://developers.google.com/machine-learning/crash-course/reducing-loss/gradient-descent)

# Issues

- Algorithm can struggle with leakage on blank areas of Content Image.
- Depending on images, last epochs can be overdone, look at earlier epochs for better results.
- Algorithm works best when content image presents a realistic scenery and style image is highly stylised ex. abstract paintings.
- Image processing takes a lot of time and resources, so it is very hard to create a lot of mergers in the short period of time and compare results, unless you use your GPU in processing. It is available only if you have a Nvidia graphic card.
- There is a lot of different methods of creating NST in the internet, although it is hard to distinguish "the best" one available.

# Examples
Our examples can be found in powerpoint file above readme.

# Our Thoughts

During our project we learned plenty of new things and discovered what is and how Neural style transfer works. We were guided by various sources such as stackoverflow, medium.com or github. Here are some of our thoughts regarding project:

We should start with blank backgrounds. Model has difficulties in keeping backgrounds of content images not impacted by style image. Usually what we could observe was a leakage of features from style image to background of content image. We can see that in our "pickle rick" or "hybrid of boy and morty" projects. Our thought on that are that you should avoid content images that have big parts of indistinctive colours or shapes. Otherwise a leakage is expected.

What we also found out, we were pretty surprised, model tends to blurry overdetailed spots of content image. We can observe that on our "Running rick and Pablo abstract art merge". In our content image rick and morty are running away from a bunch of colorful monsters that are very close to each other - they create sort of a crowd. Unfortunately, when we merged it with our violet, rectangular, abstract art our model blurred all of the monstered and faded colors there to make it grey. We were surprised by that, because from our first project we learned that we should avoid blank monotonous spaces. It turns out that we should also avoid overcrowded, oversaturated with colors spots. This made us think that there is some golden spot in between monotony and chaos on picture in which model works best.

We used VGG19 and build a little different program than one shown in our class notebook. It is hard to distinct one winner. We were quite happy with how our NST performs. It tends to be stronger and more harsh than one from our notebook which makes our results contain more style on content image. Although this is not a good thing in every project. We found out that our model was more likely to have a leakage of features from style image which is not desirable.

Our model performed mainly on content images of cartoons which was not a perfect setting at all. We found out that model operates best when content image is a real photo and it contains many objects that are not so close to each other eg. portrait or a landscape, and when a style image is a highly stylised painting or an image eg. abstract artworks or Van Gogh paintings. Although our settings were not perfect we think that our model did a good job. We created many merges that our friends want to print in a bigger dimensions and hang on their walls.

We wanted to thank You for opportunity to look deeper into a subject of NST and real usage of AI models.
