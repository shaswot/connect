# connect

```
eval $(ssh-agent) && ssh-add /stash/<id_rsa>

ssh -o ServerAliveInterval=60 -L xxx8:localhost:xxx8 -L xxx6:localhost:xxx6 <remote_server>

docker run --gpus all \
	--name <naam> \
	-dit \
	-p xxx8:xxx8 \
	-p xxx6:xxx6 \
	-v ~/stash:/stash \
	-e JUPYTER_TOKEN=xxxx \
	nvcr_pytorch:23.12

docker build -f ./docker/Dockerfile -t nvcr_pytorch:23.12 .
```
