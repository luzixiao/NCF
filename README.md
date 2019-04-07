# NCF
A pytorch GPU implementation of He et al. "Neural Collaborative Filtering" at WWW'17

Note that we use the two sub datasets provided by Xiangnan's [repo](https://github.com/hexiangnan/neural_collaborative_filtering/tree/master/Data).

We utilized a factor number **32**, MLP layers **3**, and posted the results in the original paper and this implementation here.
He's keras [repo](https://github.com/hexiangnan/neural_collaborative_filtering):
Models | MovieLens | Pinterest
------ | --------- | ---------
       | HR@10 | NDCG@10 | HR@10 | NDCG@10
MLP    | 0.692 | 0.425   | 0.868 | 0.542
GMF    |   -   |   -     |   -   |   -
NeuMF (without pre-training) | 0.701 | 0.425 | 0.870 | 0.549
NeuMF (with pre-training)	 | 0.726 | 0.445 | 0.879 | 0.555

This pytorch code:


## The requirements are as follows:
* python==3.6

* pandas==0.24.2

* numpy==1.16.2

* pytorch==1.0.1

* gensim==3.7.1

* tensorboardX==1.6 (mainly useful when you want to visulize the loss, see https://github.com/lanpa/tensorboard-pytorch)

## Example to run:
```
python main.py --batch_size=256 --lr=0.001 --embed_size=16
```
