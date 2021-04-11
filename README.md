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

## Developing in VS Code

To develop in vscode first install the docker extension:

![image info](./doc/kwarqs/docker_vscode_extension.png)

To update the docker image, right click the **Dockerfile** in vscode and click *Build Image...*:

![image info](./doc/kwarqs/vs_code_build_image.png)


Tag the image as **kwarqs-object-detection:latest** and press enter:

![image info](./doc/kwarqs/vs_code_build_image2.png)

To run the image right the *kwarqs-object-detection:latest* image in the docker vscode extension and click *Run Interactive*:

![image info](./doc/kwarqs/vs_code_docker_run_interactive.png)

This should launch a shell in vscode into the container:

![image info](./doc/kwarqs/vs_code_docker_shell.png)

To launch another shell, stop and start the container, and perform other actions right click the container in vscode:

![image info](./doc/kwarqs/vs_code_container.png)

## Generating the model

From the **kwarqs** directory inside the container generate the TFRecords:

```
python generate_tfrecord.py --csv_input=images/train_labels.csv --image_dir=images/train --output_path=training/content/train.record
python generate_tfrecord.py --csv_input=images/test_labels.csv --image_dir=images/test --output_path=training/content/test.record
```
