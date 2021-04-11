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