Build the image
```
docker build -t tf114 .
```

connect the image to jupyternotebook
```
docker run --gpus all --rm -it -p 8888:8888 tf114
```
