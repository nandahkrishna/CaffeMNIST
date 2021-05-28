# Caffe MNIST Example

This repository contains a LeNet Caffe Model trained on the MNIST dataset,
based on the instructions available at
https://caffe.berkeleyvision.org/gathered/examples/mnist.html.

## Dataset

The MNIST test dataset is included in this repository, in the LMDB format. It
was originally downloaded from http://yann.lecun.com/exdb/mnist and converted
to the LMDB format using Caffe's `convert_mnist_data` tool.

## Training

This model was trained using:

```shell
caffe train -solver=lenet_solver.prototxt
```

The train dataset is not included in this repository.

## Testing

Run this to test the model:

```shell
caffe test -model=lenet_train_test.prototxt -weights=lenet_iter_10000.caffemodel
```

## Performance

The model trained for 10000 iterations has a test accuracy of 98.6% and a
`softmax` loss of 0.0444183.

## License

The contents of this repository are released for unrestricted use.
