# PWCN

**PWCN** - **P**roximity-**W**eighted **C**onvolution **N**etwork
* Repo for [SIGIR 2019](https://sigir.org/sigir2019/
) paper titled "Syntax-Aware Aspect-Level Sentiment Classification with Proximity-Weighted Convolution Network" 
* [Chen Zhang](https://genezc.github.io), [Qiuchi Li](https://qiuchili.github.io) and Dawei Song.

## Requirements

* Python 3.6
* PyTorch 1.0.0
* SpaCy 2.0.18
* numpy 1.15.4

## Usage

* Download pretrained GloVe embeddings with this [link](http://nlp.stanford.edu/data/wordvecs/glove.840B.300d.zip) and extract `glove.840B.300d.txt` into `glove/`.
* Train with command, optional arguments could be found in [train.py](/train.py)
```bash
python train.py --model_name pwcn_dep --dataset laptop
```
* Infer with [infer.py](/infer.py)

## Model

We propose a proximity-weighted convolution network to offer an aspect-specific syntax-aware representation of contexts. In particular, two ways of determining proximity weight are explored, namely position proximity and dependency proximity. The representation is primarily abstracted by a bidirectional LSTM architecture and further enhanced by a proximity-weighted convolution.

An overview of our proposed model is given below

![model](/assets/sigir2019pwcn-fig1.png)

## Citation

If you use the code in your paper, please kindly star this repo and cite our paper

```bibtex
@inproceedings{Zhang:Syntax,
  author={Chen Zhang, Qiuchi Li, Dawei Song},
  title={Syntax-Aware Aspect-Level Sentiment Classification with Proximity-Weighted Convolution Network},
  year={2019},
  booktitle={SIGIR’19),}
}
```

## Credits

* Code of this repo heavily relies on [ABSA-PyTorch](https://github.com/songyouwei/ABSA-PyTorch), in which I am one of the contributors.
* For any issues or suggestions about this work, don't hesitate to create an issue or directly contact me via [gene_zhangchen@163.com](mailto:gene_zhangchen@163.com) !