# Dataset-of-Cognitive-Distortion-detection-and-Positive-Reconstruction：Chinese Dataset 

This dataset including Cognitive Distortion detection[(**CogDis.txt**)](https://github.com/405200144/Dataset-of-Cognitive-Distortion-detection-and-Positive-Reconstruction/blob/main/CogDis.txt) and Positive Reconstruction datasets[(**PRtrain.json**)](https://github.com/405200144/Dataset-of-Cognitive-Distortion-detection-and-Positive-Reconstruction/blob/main/PRtrain.json)/[(**PRtest.json**)](https://github.com/405200144/Dataset-of-Cognitive-Distortion-detection-and-Positive-Reconstruction/blob/main/PRtest.json).

## Data Collection
The corpus labeling utilizes one specialized open-source dataset, the Chinese psychological Q&A dataset [**PsyQA**](https://github.com/thu-coai/PsyQA), which is related to psychological issues and tends to contain statements with cognitive distortions.
This study aims to determine if the initial sentence input by the topic initiator is distorted, rather than the subsequent responses or discussions. The length of the sentences is restricted to between 10 and 66 characters to avoid excessively short or long and meaningless sentences.

## Annotation
Two postgraduate students with a background in psychology annotated 4,001 pieces of corpus for cognitive distortion detection based on the Burns(1999) 10 classification standard, 1129 of which were labeled as cognitive distortions, and internal consistency is **88%**.

The Positive Reconstruction rewriting task was posted on the college student social platform. A total of 85 undergraduates and postgraduates participated in the pre-writing test. Finally, 42 participants passed the test and participated in the writing task, including 17 males and 25 females, from different majors, with an average age of 22.7. Each writer is requested to compose five distinct positive strategy reconstructions for one cognitive distortion sentence and complete 5 to 10 sets, and 1,900 sentences were collected in total.

## Data Quality
In addition to using a pre-test to ensure that writers clearly understand the writing task, we also conducted a 5-classification experiment, a sentiment assessment, and a manual evaluation to verify the quality of the writing. In the five-classification experiment, we split the training and test sets in a 4:1 ratio, using [RoBERTa-wwm-ext](https://github.com/ymcui/Chinese-BERT-wwm) as the pre-trained model. The Accuracy reached **82.85\%** indicating that writers can compose different positive sentences based on various strategies. Furthermore, we used [SnowNLP](https://github.com/isnowfy/snownlp) for sentiment analysis of the corpus, and the results showed a significant increase in positivity for manually written content. The average sentiment score of the original sentences was 0.715, while that of the manually written content was 0.958. In the manual evaluation, we randomly selected 10 sets of negative sentences and their corresponding positive rewrites for a five-point Likert scale rating. A total of 29 evaluation feedbacks from non-research-related personnel were received, and the results showed that the average scores for manual writing were all higher than 4, for more details please read our paper.

## Citation
```
@inproceedings{lin-etal-2024-detection,
    title = "Detection and Positive Reconstruction of Cognitive Distortion Sentences: {M}andarin Dataset and Evaluation",
    author = "Lin, Shuya  and
      Wang, Yuxiong  and
      Dong, Jonathan  and
      Ni, Shiguang",
    editor = "Ku, Lun-Wei  and
      Martins, Andre  and
      Srikumar, Vivek",
    booktitle = "Findings of the Association for Computational Linguistics ACL 2024",
    month = aug,
    year = "2024",
    address = "Bangkok, Thailand and virtual meeting",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.findings-acl.399",
    pages = "6686--6701",
}
```
