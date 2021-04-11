## Installation

Clone this repo and cd into to it:

```
git clone https://github.com/frc2423/tensorflow-object-detection-example.git
cd tensorflow-object-detection-example
```

From the **tensorflow-object-detection-example** directory run these commands:

```
git clone https://github.com/tensorflow/models.git
docker build -f ./Dockerfile -t kwarqs-object-detection .
```

## Running

```
docker run -it kwarqs-object-detection
```

To access the running container first get its name by running ```docker ps``` in the terminal:

![image info](./doc/kwarqs/docker_ps.png)

And then run ```docker exec -it [container name] /bin/bash```:

![image info](./doc/kwarqs/docker_exec.png)
