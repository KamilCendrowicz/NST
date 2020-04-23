During our project we learned plenty of new things and discovered what is and how Neural style transfer works. We were guided by various sources such as stackoverflow, medium.com or github. Here are some of our thoughts regarding project:

We should start with blank backgrounds. Model has difficulties in keeping backgrounds of content images not impacted by style image. Usually what we could observe was a leakage of features from style image to background of content image. We can see that in our "pickle rick" or "hybrid of boy and morty" projects. Our thought on that are that you should avoid content images that have big parts of indistinctive colours or shapes. Otherwise a leakage is expected.

What we also found out, we were pretty surprised, model tends to blurry overdetailed spots of content image. We can observe that on our "Running rick and Pablo abstract art merge". In our content image rick and morty are running away from a bunch of colorful monsters that are very close to each other - they create sort of a crowd. Unfortunately, when we merged it with our violet, rectangular, abstract art our model blurred all of the monstered and faded colors there to make it grey. We were surprised by that, because from our first project we learned that we should avoid blank monotonous spaces. It turns out that we should also avoid overcrowded, oversaturated with colors spots. This made us think that there is some golden spot in between monotony and chaos on picture in which model works best. 

We used VGG19 and build a little different program than one shown in our class notebook. It is hard to distinct one winner. We were quite happy with how our NST performs. It tends to be stronger and more harsh than one from our notebook which makes our results contain more style on content image. Although this is not a good thing in every project. We found out that our model was more likely to have a leakage of features from style image which is not desirable.

Our model performed mainly on content images of cartoons which was not a perfect setting at all. We found out that model operates best when content image is a real photo and it contains many objects that are not so close to each other eg. portrait or a landscape, and when a style image is a highly stylised painting or an image eg. abstract artworks or Van Gogh paintings.
Although our settings were not perfect we think that our model did a good job. We created many merges that our friends want to print in a bigger dimensions and hang on their walls.

We wanted to thank You for opportunity to look deeper into a subject of NST and real usage of AI models.

Jakub Walczak 38682
Kamil Cendrowicz 38649
