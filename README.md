# kdd2024rebuttal

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
| SCET-as*      | 2.729 ± 1.154     | 1.793 ± 0.142     | 1.830 ± 0.194     | 2.106 ± 1.006     | 1.147 ± 0.022     | 1.315 ± 0.155     | 1.820 ± 0.821     |
| SCET-a*       | 2.360 ± 0.716     | 2.176 ± 0.853     | 2.211 ± 0.854     | 2.021 ± 0.272     | 1.548 ± 0.153     | 1.508 ± 0.229     | 1.971 ± 0.679     |
| SCET-c*       | 4.678 ± 0.812     | 3.236 ± 0.591     | 5.236 ± 0.878     | 4.021 ± 0.537     | 3.228 ± 0.587     | 3.638 ± 0.615     | 4.006 ± 1.007     |


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
| SCET-as*      | 12.017 ± 1.392     | 12.686 ± 1.018     | 14.132 ± 0.586     | 13.841 ± 0.595     | 13.169 ± 1.286     |
| SCET-a*       | 11.155 ± 1.873     | 11.383 ± 1.495     | 11.938 ± 1.263     | 12.172 ± 1.339     | 11.662 ± 1.566     |
| SCET-c*       | 13.201 ± 0.405     | 12.762 ± 0.332     | 13.187 ± 0.110     | 13.556 ± 0.149     | 13.177 ± 0.395     |
