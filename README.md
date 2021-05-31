**General Multi-label Image Classification with Transformers**<br/>
Jack Lanchantin, Tianlu Wang, Vicente Ordóñez Román, Yanjun Qi<br/>
[arXiv preprint 2020](https://arxiv.org/abs/2011.14027)<br/>




## Training and Running Models ##

Python version 3.7 is required and all major packages used and their versions are listed in `requirements.txt`.

### COCO80 ###
Download COCO data (19G)
```
wget http://cs.virginia.edu/~jjl5sw/data/vision/coco.tar.gz
mkdir -p data/
tar -xvf coco.tar.gz -C data/
```

Train New Model
```
python main.py  --batch_size 16  --lr 0.00001 --optim 'adam' --layers 3  --dataset 'coco' --use_lmt --dataroot data/
```


### VOC20 ###
Download VOC2007 data (1.7G)
```
wget http://cs.virginia.edu/~jjl5sw/data/vision/voc.tar.gz
mkdir -p data/
tar -xvf voc.tar.gz -C data/
```

Train New Model
```
python main.py  --batch_size 16  --lr 0.00001 --optim 'adam' --layers 3  --dataset 'voc' --use_lmt --grad_ac_step 2 --dataroot data/
```


## Citing ##

```bibtex
@article{lanchantin2020general,
  title={General Multi-label Image Classification with Transformers},
  author={Lanchantin, Jack and Wang, Tianlu and Ordonez, Vicente and Qi, Yanjun},
  journal={arXiv preprint arXiv:2011.14027},
  year={2020}
}
```
