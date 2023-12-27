# GNN-IR: Examining Graph Neural Networks for Influencer Recommendations in Social Media Marketing
This repository is to supplement the paper "GNN-IR: Examining Graph Neural Networks for Influencer Recommendations in Social Media Marketing".


## Abstract
With the notable growth of the Internet, a number of platforms have emerged and at- tracted an enormous number of users. Based on the impact of these platforms, some ‘influencers’ are highlighted. These influencers wield significant power, shaping con- sumer behavior. This influence spawned the concept of influencer marketing, where companies leverage these personalities to advertise their products. YouTube stands out as a prominent platform in this trend. However, considering the limited number of influencers and their concepts, the majority of companies, which hope to conduct their marketing campaigns with influencers face challenges in identifying suitable in- fluencers for their campaigns. With this trend, we introduce GNN-IR, a graph neural network for influencer recommendation, based on the connections between companies and influencers of YouTube, one of the largest content platforms. Through building GNN-IR, we conducted a data-driven approach using suitable dataset collected by our- selves. We collected 25,174 relationship data between advertiser and influencer in total, composing 1,886 unique advertisers and 3,812 unique YouTube influencers. The dataset comprises various modalities such as image, text, and several metadata. The data was collected through websites: YouTube and ugwanggi. Ugwanggi contains the relationship between advertisers and influencers through their information. YouTube represents more detailed information on influencers. We construct a bipartite graph rep- resenting this linked data through torch geometric. The recommendation is performed based on link prediction. Top-k influencers are recommended to an advertiser using the connection probability between two nodes obtained through link prediction. We veri- fied GNN-IR performance based on various evaluation metrics. In link prediction, we used Accuracy, Precision, Recall, and F1-score. Furthermore, in recommendation, we used Precision@k, Recall@k, and F1-score@k for evaluation. By utilizing profile im- ages in YouTube, keyword features, metadata, and sentiment from YouTube comments with GNN-IR, 96.51% Precision (k=1) and 93.68% (k=10) are achieved. Based on the experimental results, several implications and limitations are presented.


## Overview of our framework
<img alt="GNN_IR (1)" src="https://github.com/dxlabskku/GNN-IR/assets/121244986/81ce440f-80ab-4d9c-ac2e-2d35a6d71d04" width="636.75" height="600">
<br>
<strong>Figure 1 : GNN-IR framework </strong>
<br>



## Dataset
We constructed a sponsorship dataset capturing the relationship between commercial sponsors and YouTube creators sourced from _Ugwanggi_, a platform specifically designed for checking sponsorship advertisement lists on YouTube. Encompassing samples dating from 2016 to September 5th, 2023, the dataset contains details such as the sponsor's name, YouTube creator's name, upload date of videos, sponsor categories, and keywords associated with YouTube creators. In addition, our data collection extended to YouTube to gather more nuanced information about YouTube creators, which includes the number of subscribers, total video count, overall view counts, creators' profile images, and video IDs. After pre-processing, our dataset consisted of 25,174 links between advertisers and influencers. Among these, we identified 1,886 unique advertisers and 3,812 unique YouTube influencers. The link between them represents whether advertiser entrusted the advertisement to influencers. During our analysis, we noticed that the variations in the minimum and maximum values or standard deviations of influencers' subscribers, video views, and the number of video features are quite substantial. To address this, we proceeded with additional feature extraction to normalize these features. The statistical description of our dataset is follows: 


| Feature         | Min | Max          | Mean(sd)                  | Median       |
|----------|-----|--------------|---------------------------|--------------|
| Subscriber(SS)       | 5   | 1,390,000    | 180,334.31 (212,078.89)  | 105,000      |
| Views (VW)       | 965 | 11,946,595,208 | 157,049,875.86 (529,003,445.42) | 30,533,582   |
| Videos (VD)       | 3   | 85,000       | 671.75 (2521.64)          | 287          |
| Average View by subscribers (AVS)      | 0.61 | 29,109       | 1,044.76 (2225.97)        | 323.69       |
| Average View by Videos (AVV)      | 60.31 | 21,546,560   | 299,430 (712,458.68)      | 102,123.46   |
| AVS Rank (AVSR) | 1   | 10           | 1.16 (0.66)               | 1            |
| AVV Rank (AVVR) | 1   | 10           | 1.02 (0.25)               | 1            |
| Subscriber Rank (SR)   | 1   | 10           | 1.90 (1.46)               | 1            |
| Video Rank (VDR)  | 1   | 10           | 1.04 (0.43)               | 1            |
| View Rank (VWR)      | 1   | 10           | 1.03 (0.37)               | 1            |
| Negative Comment Sentiment (NCS)      | 0   | 0.93         | 0.27 (0.16)               | 0.23         |
| Positive Comment Sentiment (PCS)      | 0   | 0.97         | 0.71 (0.16)               | 0.76         |
| NCS Rank (NCSR) | 1   | 5            | 1.98 (0.94)               | 2            |
| PCS Rank (PCSR)     | 1   | 5            | 4.19 (0.92)               | 4            |





## Implementation detail
TBD


## Reference
TBD
