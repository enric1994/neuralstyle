# Neuralstyle
Dockerized version of https://github.com/cysmith/neural-style-tf

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