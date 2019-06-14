During the first month of my PhD I worked on the style transfer technique applied to videos. The objective is transform the news into a "cartoonized" video for kids by transferring the style of a cartoon.

The style transfer process requires 2 photos:

* The target: the image that we want to represent with another style. All the colors and textures will be lost in the process, however the contents will survive to the output image.
* The style: the image with the textures and colors that will be transferred to the output.

The following video transfer the style from the "The Powerpuff Girls" to the weather forecast:

<iframe width="560" height="315" src="https://www.youtube.com/embed/uSIRT_fGo9E" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

# Usage
Having Docker, Docker Compose, NVIDIA-Docker and a NVIDIA GPU run:

`docker-compose -f docker/docker-compose.yml run neuralstyle bash`

Then, use the neural_style.py script on images/videos:

```
python neural_style.py --content_img golden_gate.jpg \
                       --style_imgs starry-night.jpg \
                       --max_size 500 \
                       --max_iterations 100 \
                       --verbose;
``` 


This repository is a Dockerized version of https://github.com/cysmith/neural-style-tf
