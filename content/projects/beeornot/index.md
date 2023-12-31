---
title: "A Bee or Not a Bee?"
date: "2023-24-08"
draft: false
socialShare: true
math: true
gradio: true
weight: 1
cover:
  src: ./bee_yellow.jpg
  caption: A bee!
---

Bees, wasps, and hoverflies look pretty similar. It can be easy to forget who's who. Hover flies don't sting! Bees pollinate flowers, and make honey. Wasps well... Let's just hope they're doing their bit. 

I trained an image classifier that can help. It's **95 % accurate** on my validation set! <!--more--> **Note:** pictures from your camera will be a little harder.


<br>

<div style="display: flex;">
    {{< figure src="./bee_purpleflower.jpg" alt="Bee" >}}
    {{< figure src="./testhoverfly_whiteflower.jpg" alt="Hoverfly" >}}
    {{< figure src="./testwasp.jpg" alt="Wasp" >}}
</div>

<br>

<style>
img {
  object-fit: cover;
  height: 250px;
}
</style>


## Try it out!

{{< warning Disclaimer>}}
This is a demo model - use at your own risk. Stay safe out there, don't get stung!
{{< /warning >}}

Here is a [link to a demo on my Huggingface spaces](https://huggingface.co/spaces/Ben-orli/a-bee-or-not-a-bee) with demo images you can drag and drop, or upload your own images. I highly recommend clicking the link as it's fun and intuitive.

If you love this site so much you don't want to leave, please don't fear, you can upload your images with the button below:

{{< beeupload >}}

This button accesses my model through an API and passes the result right back to you here on the site.

## Info for Nerds

The classifier is a neural network I **trained locally on my GPU** using **fastai/PyTorch**. I downloaded the images **from DuckDuckGo using Python** then cleaned the images myself—turns out there are a lot of cartoon bees on the internet. I was able to train it to 95 % accuracy using under 600 images using a combination of **data augmentation** and **transfer learning**.