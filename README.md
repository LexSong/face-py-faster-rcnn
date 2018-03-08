# Face Detection with the Faster R-CNN (on Windows)

Build [face-py-faster-rcnn](https://github.com/playerkk/face-py-faster-rcnn) on Windows, based on [py-faster-rcnn-windows](https://github.com/MrGF/py-faster-rcnn-windows) and [caffe-rfcn](https://github.com/daijifeng001/caffe-rfcn).

### Install Steps

1. Build caffe-rfcn
2. Build the Cython modules under `lib`
3. Prepare data and pre-trained model
4. Demo

### Build Caffe-rfcn

**Build environments**: Visual Studio 2013, CUDA 7.5, Python 2.7

Clone and build [caffe-rfcn](https://github.com/daijifeng001/caffe-rfcn).

Copy and rename `caffe-rfcn\Build\x64\Release\pycaffe` to `face-py-faster-rcnn-windows\caffe-fast-rcnn\python`.

Check [caffe-rfcn](https://github.com/daijifeng001/caffe-rfcn) for more details.

### Build the Cython Modules

**NOTE** May need extra python dependecies

    cd face-py-faster-rcnn-windows\lib
    python setup.py build_ext --inplace
    python setup_cuda.py build_ext --inplace

### Prepare Data and Pre-trained Model

Copy model to `output\faster_rcnn_end2end\train\vgg16_faster_rcnn_iter_80000.caffemodel`

Copy FDDB to `data\FDDB\FDDB-folds` and `data\FDDB\originalPics`

Check [face-py-faster-rcnn](https://github.com/playerkk/face-py-faster-rcnn) for more details.

### Demo

**NOTE** May need extra python dependecies

    cd face-py-faster-rcnn-windows
    python tools\run_face_detection_on_fddb.py

