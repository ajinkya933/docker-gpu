Build the image
```
docker build -t tf114 .
```

connect the image to jupyternotebook
```
docker run --gpus all --rm -it -p 8888:8888 tf114
```
to attach external volume (used incase to retain data)
```
docker run --mount source=tf114disk,target=/tf --gpus all --rm -it -p 8888:8888 tf114
```
then go to :
127.0.0.1:8888
and paste the token from terminal to gain access
