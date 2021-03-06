## MetaSleepLearner (https://ieeexplore.ieee.org/document/9258375)
##### N. Banluesombatkul et al., "MetaSleepLearner: A Pilot Study on Fast Adaptation of Bio-signals-Based Sleep Stage Classifier to New Individual Subject Using Meta-Learning," in IEEE Journal of Biomedical and Health Informatics, doi: 10.1109/JBHI.2020.3037693.
##### This source code belongs to INTERFACES (BRAIN lab @ IST, VISTEC, Thailand)

## Datasets
Five publicly datasets were used to evaluate our method including
* MASS (http://massdb.herokuapp.com/en/) - Permission required
* SleepEDF (https://physionet.org/content/sleep-edf/1.0.0/)
* ISRUC (https://sleeptight.isr.uc.pt)
* UCD (https://physionet.org/content/ucddb/1.0.0/)
* CAP (https://physionet.org/content/capslpdb/1.0.0/)

[All of them should be prepared and put in /data - only MASS datasets were pre-processed using bandpass filters as described in our paper]

## Algorithm source code (/src)
* set up configuration i.e. data path, model hyperparameters, etc. in ```configure.py```
* meta-train (our approach) ```python MAML.py```
* normal pre-train (baseline) ```python NormalPretrain.py```
* fine-tune: configure and run ```python FinetuneCNNKFolds.py```
* evaluate: put list of fine-tune weights path and run notebook ```FinetuneAndTestOnBestHyperparams-List.ipynb```

## Other configuration: 
* Every file: set GPU# before running
* bot.py: add your chat ID and bot token (if you want to have notification, otherwise just remove all lines calling it.)

## Citation
To cite [our paper](https://doi.org/10.1109/JBHI.2020.3037693),

```
@ARTICLE{9258375,
  author={N. {Banluesombatkul} and P. {Ouppaphan} and P. {Leelaarporn} and P. {Lakhan} and B. {Chaitusaney} and N. {Jaimchariya} and E. {Chuangsuwanich} and W. {Chen} and H. {Phan} and N. {Dilokthanakul} and T. {Wilaiprasitporn}},
  journal={IEEE Journal of Biomedical and Health Informatics}, 
  title={MetaSleepLearner: A Pilot Study on Fast Adaptation of Bio-signals-Based Sleep Stage Classifier to New Individual Subject Using Meta-Learning}, 
  year={2020},
  volume={},
  number={},
  pages={1-1},
  doi={10.1109/JBHI.2020.3037693}}
```
