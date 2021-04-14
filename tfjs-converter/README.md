# Converter

Instructions can be found here: https://github.com/tensorflow/tfjs/tree/master/tfjs-converter

### Running

Create the docker image:

```
docker build -f .\Dockerfile -t tfjs-converter .
```

In the docker container:

```
tensorflowjs_converter --input_format=tf_saved_model --output_format=tfjs_graph_model --signature_name=serving_default --saved_model_tags=serve ./inference_graph/saved_model ./web_model
```