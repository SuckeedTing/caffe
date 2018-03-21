make all -j8
make test -j8
make runtest -j8
make pycaffe -j8
make matcaffe -j8
(1)
cd $densenetcaffe_root
./data/cifar10/get_cifar10.sh
./examples/cifar10/create_cifar10.sh
(2)
By default make_densenet.py generates a DenseNet with Depth L=40, Growth rate k=12 and Dropout=0.2. To experiment with different settings, change the code accordingly (see the comments in the code). Example prototxt files are already included. Use python densenet_make.py to generate new prototxt files.
(3) change the caffe path in train.sh. Then use "sh train.sh" to train a DenseNet

