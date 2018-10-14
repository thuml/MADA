# MADA
Code release for "Multi-Adversarial Domain Adaptation" (AAAI 2018)

## Modification on Caffe
- Add "OuterProduct" layer to calculate weighted feature to input to each domain adversarial network;

## Datasets
### Office-31
The list files of Office-31 dataset are in [office](./data/office) directory. You can download the original images [here](https://people.eecs.berkeley.edu/~jhoffman/domainadapt).

## Training
The training command is as follows
```
./build/tools/caffe train -solver models/mada/solver.prototxt -weights ./models/bvlc_reference_caffenet/bvlc_reference_caffenet.caffemodel -gpu gpu_id
``` 
You need to download the reference\_caffenet model [here](http://dl.caffe.berkeleyvision.org/bvlc_reference_caffenet.caffemodel).

For different tasks, you need to set the "test\_iter" parameter in the solver file as the size of the target dataset. For example, when "webcam" is used as target domain, you need to set the "test\_iter" parameter as 795.

## Contact
If you have any problem about our code, feel free to contact 
### caozhangjie14@gmail.com 
### peizhyi@gmail.com
### or describe your problem in Issues.
