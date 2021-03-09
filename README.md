# SKER
The source code of the COLING 2020 paper "[Synonym Knowledge Enhanced Reader for Chinese Idiom Reading Comprehension](https://www.aclweb.org/anthology/2020.coling-main.329/)".

# Requirements
See requirement.txt for details

- allennlp==0.8.5
- torch==1.1.0
- pytorch-transformers==1.1.0

# Usage

**Training**
```
export PROJECT_ROOT='/path/to/project'
export CUDA_VISIBLE_DEVICES=0,1,2,3
allennlp train config/sker.jsonnet -s /path/to/save --include-package src
```

**Testing**
```
allennlp predict /path/to/model.tar.gz data/evaluated_ChID_dataset.txt --output-file /path/to/output --silent --cuda-device 0 --use-dataset-reader --predictor chid --include-package src --batch-size 16
```

# Citation
If you used the datasets or code, please cite our paper:
```
@inproceedings{SKER2020,
  author    = {Siyu Long and
               Ran Wang and
               Kun Tao and
               Jiali Zeng and
               Xinyu Dai},
  editor    = {Donia Scott and
               N{\'{u}}ria Bel and
               Chengqing Zong},
  title     = {Synonym Knowledge Enhanced Reader for Chinese Idiom Reading Comprehension},
  booktitle = {Proceedings of the 28th International Conference on Computational
               Linguistics, {COLING} 2020, Barcelona, Spain (Online), December 8-13,
               2020},
  pages     = {3684--3695},
  publisher = {International Committee on Computational Linguistics},
  year      = {2020},
  url       = {https://www.aclweb.org/anthology/2020.coling-main.329/},
  timestamp = {Fri, 18 Dec 2020 16:04:15 +0100},
  biburl    = {https://dblp.org/rec/conf/coling/LongWTZD20.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```
