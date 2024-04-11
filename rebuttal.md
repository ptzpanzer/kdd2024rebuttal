# kdd2024rebuttal

We complement new baseline models and ablation studies on the two real-world datasets, SAQN and Marine. 

The new baseline includes GraphSAGE and PE-GraphSAGE. 

The ablation study includes 

  (1) the proposed model without input centering (SCET-w/o c), 
  
  (2) the proposed model without auxiliary tasks (SCET-w/o a), and 
  
  (3) the proposed model without the 2-stage design and auxiliary task (SCET-w/o a&s), which is a vanilla Transformer.

The results are as follows:


| Model         | Marine-0          | Marine-1          | Marine-2          | Marine-3          | Marine-4          | Marine-5          | Overall           |
|---------      |----------         |----------         |----------         |----------         |----------         |----------         |----------         |
| IDW           | 4.805             | 1.229             | 4.325             | 2.744             | 2.899             | 2.086             | 3.015             |
| GCN           | 8.114 ± 0.813     | 7.218 ± 0.344     | 6.190 ± 0.239     | 5.808 ± 2.597     | 3.482 ± 0.313     | 2.274 ± 0.487     | 5.514 ± 2.279     |
| PE-GCN        | 8.006 ± 0.417     | 3.711 ± 0.437     | 6.667 ± 0.579     | 3.017 ± 0.290     | 2.005 ± 0.314     | 1.804 ± 0.263     | 4.202 ± 2.364     |
| PE-GAT        | 5.540 ± 1.058     | 2.609 ± 0.574     | 4.464 ± 0.191     | 3.065 ± 0.317     | 2.901 ± 0.397     | 1.945 ± 0.293     | 3.421 ± 1.309     |
| GraphSAGE     | 3.791 ± 0.659     | 2.512 ± 0.671     | 3.877 ± 1.126     | 3.313 ± 0.870     | 2.440 ± 0.439     | 2.083 ± 0.673     | 3.003 ± 1.053     |
| PE-GraphSAGE  | 3.942 ± 0.357     | **1.105 ± 0.233** | 4.703 ± 0.254     | 2.074 ± 0.157     | 1.576 ± 0.248     | **1.034 ± 0.046** | 2.406 ± 1.434     |
| SCET*         | **2.143 ± 0.639** | 1.767 ± 0.339     | **2.499 ± 0.174** | **2.055 ± 0.395** | **1.445 ± 0.189** | 1.630 ± 0.195     | **1.923 ± 0.476** |
|---------      |----------         |----------         |----------         |----------         |----------         |----------         |----------         |
| SCET-w/o a&s  | 2.729 ± 1.154     | 1.793 ± 0.142     | 1.830 ± 0.194     | 2.106 ± 1.006     | 1.147 ± 0.022     | 1.315 ± 0.155     | 1.820 ± 0.821     |
| SCET-w/o a    | 2.360 ± 0.716     | 2.176 ± 0.853     | 2.211 ± 0.854     | 2.021 ± 0.272     | 1.548 ± 0.153     | 1.508 ± 0.229     | 1.971 ± 0.679     |
| SCET-w/o c    | 4.678 ± 0.812     | 3.236 ± 0.591     | 5.236 ± 0.878     | 4.021 ± 0.537     | 3.228 ± 0.587     | 3.638 ± 0.615     | 4.006 ± 1.007     |


| Model         | SAQN-0             | SAQN-1             | SAQN-2             | SAQN-3             | Overall            |
|----------     |----------          |----------          |---------           |---------           |---------           |
| IDW           | 16.890             | 15.266             | 15.661             | 18.211             | 16.507             |
| GCN           | 11.649 ± 0.819     | 12.537 ± 0.938     | 12.645 ± 0.727     | 13.382 ± 0.714     | 12.553 ± 0.947     |
| PE-GCN        | 11.101 ± 0.420     | 11.873 ± 0.394     | 12.796 ± 0.590     | 13.407 ± 0.741     | 12.294 ± 1.009     |
| PE-GAT        | 12.867 ± 0.522     | 12.312 ± 0.756     | 12.996 ± 0.642     | 13.255 ± 0.770     | 12.858 ± 0.699     |
| GraphSAGE     | 11.721 ± 0.552     | 11.681 ± 0.481     | **11.609 ± 0.731** | 12.734 ± 0.748     | 11.936 ± 0.788     | 
| PE-GraphSAGE  | **7.251 ± 0.747**  | 12.251 ± 1.672     | 12.242 ± 2.269     | **9.253 ± 1.018**  | **10.249 ± 2.622** | 
| SCET*         | 9.962 ± 2.168      | **10.402 ± 1.969** | 11.615 ± 1.003     | 11.879 ± 1.394     | 10.965 ± 1.718     |
|---------      |----------          |----------          |----------          |----------          |----------          |
| SCET-w/o a&s  | 12.017 ± 1.392     | 12.686 ± 1.018     | 14.132 ± 0.586     | 13.841 ± 0.595     | 13.169 ± 1.286     |
| SCET-w/o a    | 11.155 ± 1.873     | 11.383 ± 1.495     | 11.938 ± 1.263     | 12.172 ± 1.339     | 11.662 ± 1.566     |
| SCET-w/o c    | 13.201 ± 0.405     | 12.762 ± 0.332     | 13.187 ± 0.110     | 13.556 ± 0.149     | 13.177 ± 0.395     |


## Analysis of GraphSAGE and PE-GraphSAGE:

Overall, GraphSAGE and PE-GraphSAGE perform better than other baselines.

However, GraphSAGE still cannot compete with SCET performance-wise regarding average performance and variance.

The average performance of PE-GraphSAGE is also weaker than SCET on the Marine dataset but stronger on the SAQN dataset. However, it must also be pointed out that the overall variance of PE-GraphSAGE is much more significant than SCET and GraphSAGE on both datasets. This further confirms our analysis of finding 4 in the original article 5.2: introducing information related to absolute coordinates is a double-edged sword because this information is not necessarily suitable for extrapolating other coordinates. It must be emphasized that in the SAQN data set, only four official sites are qualified as ground truth. Three of them are in the city center, closely surrounded by many sensors, and the last one is in the suburbs. This could lead the PE-based models to benefit due to their preference for different target locations.

## Ablation Study analysis:

By comparing the results of SCET-w/o c and SCET (the only difference is whether input centering is used), it is obvious that input centering contributes to performance improvement. This is because the Transformer has powerful fitting capabilities and can easily overfit information related to the absolute position of the input, which, due to the ordinarily small size of the WSN datasets, may not be good for extrapolation to unseen coordinates.

By comparing the results of SCET-w/o a and SCET (the only difference is whether the auxiliary task is used), it is obvious that the auxiliary task contributes to performance improvement. This is because the auxiliary task introduces additional prior knowledge to the Transformer: the Context Auxiliary Task guides the model to pay attention to the relationship between coordinates through the IDW interpolation results. The Environment Auxiliary Task interprets the difference between the Label and IDW interpolation results as the influence from other Support Observed Property readings. It prompts the model to encode the Support Observed Property reading sequence into an Embedding suitable for bridging the difference between the two.

By comparing the results of SCET-w/o a and SCET-w/o a&s (the only difference is whether the 2-stage design is used), we found that the 2-stage design improves the performance on the SAQN dataset but has some counter-effects on the Marine dataset. This is because the primary purpose of the 2-stage design is to reduce the impact of noise in the data. The SAQN data set has not undergone any quality checks, so this module has a noticeable effect, while the readings in the Marine dataset all passed the quality check. In GNN-based models, a node only accepts information from its neighbor nodes in each round of information transfer. Therefore, the noise from neighbor nodes with two hops and above is weakened through multiple rounds of transmission, while the noise of more remote nodes cannot be transmitted to this node at all. The inspiration for the 2-stage design comes from this feature: The Transformer adaptively learns attention through the entire token sequence, which causes it to be affected by all noise in the entire token sequence. By physically separating Support Observed Property tokens and Target Observed Property tokens, we hope to weaken this phenomenon. When there is no noise in the data itself, the 2-stage design will cause the Transformer to be unable to directly learn the attention between Support Observed Property tokens and Target Observed Property tokens, resulting in potential performance degradation. Fortunately, according to the overall results on the Marine dataset, the performance drop is not very significant, and the 2-stage design still plays a role in combating over-fitting, showing that the overall std is significantly lower.
