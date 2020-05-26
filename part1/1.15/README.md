# Random Jokes, Dockerized
An web application that tells jokes!
[Click here to visit the image's Docker Hub page](https://hub.docker.com/r/amadeuspham/random-jokes)

To pull the image

```bash
docker pull amadeuspham/random-jokes
```

To run start the app in a container, run

```bash
docker run -it --rm -p 3000:3000 random-jokes
```

The app would be available in localhost:3000