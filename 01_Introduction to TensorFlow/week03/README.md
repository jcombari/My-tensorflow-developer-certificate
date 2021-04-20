# My-tensorflow-developer-certificate

Coding convolutions and pooling layers
The concepts introduced in this video are available as [Conv2D](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Conv2D) layers and [MaxPooling2D](https://www.tensorflow.org/api_docs/python/tf/keras/layers/MaxPool2D) layers in TensorFlow. You’ll learn how to implement them in code in the next video…


For more details on convolutions and how they work, there's a great set of resources [here](https://www.youtube.com/playlist?list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF).

Learn more about convolutions
You’ve seen how to add a convolutional 2d layer to the top of your neural network in the previous video. If you want to see more detail on how they worked, check out the playlist at [https://bit.ly/2UGa7uH](https://www.youtube.com/playlist?list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF).

Now let’s take a look at adding the pooling, and finishing off the convolutions so you can try them out…


![plot](https://github.com/jcombari/My-tensorflow-developer-certificate/blob/main/Introduction%20to%20TensorFlow%20for%20Artificial%20Intelligence%2C%20Machine%20Learning%2C%20and%20Deep%20Learning/week03/img/01_implementing%20pooling%20layers.PNG)

 This when you think about it, means that you can't use a one pixel margin all around the image, so the output of the convolution will be two pixels smaller on x, and two pixels smaller on y. If your filter is five-by-five for similar reasons, your output will be four smaller on x, and four smaller on y. So, that's y with a three by three filter, our output from the 28 by 28 image, is now 26 by 26, we've removed that one pixel on x and y, and each of the borders. So, next is the first of the max-pooling layers. Now, remember we specified it to be two-by-two, thus turning four pixels into one, and having our x and y. So, now our output gets reduced from 26 by 26, to 13 by 13. The convolutions will then operate on that, and of course, we lose the one pixel margin as before, so we're down to 11 by 11, add another two-by-two max-pooling to have this rounding down, and went down, down to five-by-five images. So, now our dense neural network is the same as before, but it's being fed with five-by-five images instead of 28 by 28 ones. But remember, it's not just one compress five-by-five image instead of the original 28 by 28, there are a number of convolutions per image that we specified, in this case 64. So, there are 64 new images of five-by-five that had been fed in. Flatten that out and you have 25 pixels times 64, which is 1600. So, you can see that the new flattened layer has 1,600 elements in it, as opposed to the 784 that you had previously. This number is impacted by the parameters that you set when defining the convolutional 2D layers. Later when you experiment, you'll see what the impact of setting what other values for the number of convolutions will be, and in particular, you can see what happens when you're feeding less than 784 over all pixels in. Training should be faster, but is there a sweet spot where it's more accurate? Well, let's switch to the workbook, and we can try it out for ourselves.
 
 
# Try it for yourself
[Here’s](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%206%20-%20Lesson%202%20-%20Notebook.ipynb) the notebook that Laurence was using in that screencast. To make it work quicker, go to the ‘Runtime’ menu, and select ‘Change runtime type’. Then select GPU as the hardware accelerator! 

Work through it, and try some of the exercises at the bottom! It's really worth spending a bit of time on these because, as before, they'll really help you by seeing the impact of small changes to various parameters in the code. You should spend at least 1 hour on this today!

Once you’re done, go onto the next video and take a look at some code to build a convolution yourself to visualize how it works!


# Experiment with filters and pools
To try this [notebook](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%206%20-%20Lesson%203%20-%20Notebook.ipynb) for yourself, and play with some convolutions, here’s the notebook. Let us know if you come up with any interesting filters of your own! 

As before, spend a little time playing with this notebook. Try different filters, and research different filter types. There's some fun information about them here: https://lodev.org/cgtutor/filtering.html

# Week 3 Resources
We've put the notebooks that you used this week into GitHub so you can download and play with them. 

[Adding Convolutions to Fashion MNIST](https://github.com/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%206%20-%20Lesson%202%20-%20Notebook.ipynb)

[Exploring how Convolutions and Pooling work](https://github.com/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%206%20-%20Lesson%203%20-%20Notebook.ipynb)
