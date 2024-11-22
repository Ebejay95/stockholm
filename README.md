# stockholm

docker build -t stockholm .
docker run -it --rm -v $(pwd):/app stockholm
docker ps -a
docker images
docker rm

pip install -r requirements.txt
./stockholm