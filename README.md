# LeBenchmark: a reproducible framework for assessing SSL from speech

 Self-Supervised Learning (SSL) using huge unlabeled data has been successfully explored for image and natural language processing. Recent works also investigated SSL from speech. They were notably successful to improve performance on downstream tasks such as automatic speech recognition (ASR). While these works suggest it is possible to reduce dependence on labeled data for building efficient speech systems, their evaluation was mostly made on ASR and using multiple and heterogeneous experimental settings (most of them for English). This renders difficult the objective comparison between SSL approaches and the evaluation of their impact on building speech systems.
 
  In this repository, we propose **LeBenchmark**: a reproducible framework for assessing SSL from speech. 
  It not only includes ASR (high and low resource) tasks but also spoken language understanding, speech translation and emotion recognition. Also, it targets speech technologies in a language different than English: French. 
  SSL models of different sizes are trained from carefully sourced and documented datasets.
  
  
Our pre-trained SSL models for French are available through this HuggingFace link: https://huggingface.co/LeBenchmark

Our benchmark tasks are available on the following directories:

[ASR: Automatic Speech Recognition](https://github.com/LeBenchmark/NeurIPS2021/tree/main/ASR)

[SLU: Spoken Language Understanding](https://github.com/LeBenchmark/NeurIPS2021/tree/main/SLU)

[AER: Automatic Emotion Recognition](https://github.com/LeBenchmark/NeurIPS2021/tree/main/AER)

[AST: Automatic Speech Translation](https://github.com/LeBenchmark/NeurIPS2021/tree/main/AST)

Detailed descriptions of experiments and results are given in on our paper: TBC !

