## Experiments on more baselines

We add BGRL, MASKGAE, AFGRL and COSTA as baseline and report their performance. In node classification we use public split for Cora/CiteSeer and PubMed, and 10/10/80 train/valid/test split for other datasets. Also, we train the previous "OOM" result in batched manner to show the performance.

### Experiments on clustering

| clustering | Cora  | CiteSeer | PubMed | Photo | Computer | CS    | Physics | Mean   |
|------------|-------|----------|--------|-------|----------|-------|---------|--------|
| BGRL       | 58.5  | 45.09    | 41.3   | 64.56 | 58.15    | 83.28 | 76.91   | 61.11  |
| MaskGAE    | 60.35 | 44.58    | 43.41  | 64.96 | __59.51__    | 82.89 | 76.78   | 61.78  |
| AFGRL      | 60.87 | 42.41    | 30.82  | 63.45 | 52.41    | 82    | 75.22   | 58.17  |
| COSTA      | 54.7  | 40.66    | 36.79  | 54.76 | 40.8     | 77.95 | 67.42   | 53.30  |
| GRACE      | 53.48 | 41.17    | __44.85__  | 63.14 | 55.8     | 66.4  | 65.34   | 55.74  |
| DGI        | 57.13 | 44.6     | 36.83  | 64.1  | 54.64    | 68.79 | 62.87   | 55.57  |
| CCA-SSG    | 58.12 | 31.54    | 38.92  | 65.79 | 55.29    | 80.53 | 75.62   | 57.97  |
| MVGRL      | 56.37 | 44.17    | 37.85  | 63.75 | 55.24    | 69.32 | 67.95   | 56.38  |
| GraphMAE   | 60.27 | 44.55    | 40.48  | 56.4  | 56.04    | 80.3  | 73.54   | 58.80  |
| SeeGera    | 59.81 | 45.5     | 41.27  | 58    | 56.42    | 76.6  | 77.32   | 59.27  |
| GCLFormer  | __61.15__ | __45.62__    | 39.44  | __65.87__ | 57.32    | __88.71__ | __77.6__    | __62.24__  |


### Experiments on node classification

| node      | Cora  | CiteSeer | PubMed | Photo | Computer | CS    | Physics | Mean   |
|-----------|-------|----------|--------|-------|----------|-------|---------|--------|
| BGRL      | 82.7  | 71.13    | 79.67  | 93.17 | __90.34__    | 93.31 | 95.73   | 86.58  |
| MaskGAE   | 84.3  | __73.8__     | 80.58  | 93.31 | 89.54    | 93.28 | 95.77   | 87.23  |
| AFGRL     | 83.27 | 71.35    | 79.64  | 93.22 | 89.88    | 93.27 | 95.69   | 86.62  |
| COSTA     | 84.25 | 72.47    | 80.47  | 92.56 | 88.32    | 92.95 | 95.74   | 86.68  |
| GRACE     | 81.92 | 71.23    | 80.62  | 92.15 | 86.25    | 92.93 | 95.26   | 85.77  |
| DGI       | 82.3  | 71.8     | 76.8   | 91.61 | 83.95    | 92.15 | 94.51   | 84.73  |
| CCA-SSG   | 84    | 73.1     | 81     | 93.14 | 88.74    | 93.31 | 95.38   | 86.95  |
| MVGRL     | 83.5  | 73.3     | 80.1   | 91.74 | 87.52    | 92.11 | 95.33   | 86.23  |
| GraphMAE  | 84.2  | 73.4     | 81.1   | 92.98 | 88.34    | 93.08 | 95.3    | 86.91  |
| SeeGera   | 84.3  | 73       | 80.4   | 92.81 | 88.39    | 93.84 | 95.39   | 86.88  |



### Experiments on link prediction, the ROC is reported
| ROC       | Cora  | CiteSeer | PubMed | Photo | Computer | CS    | Physics | Mean   |
|-----------|-------|----------|--------|-------|----------|-------|---------|--------|
| BGRL      | 95.23 | 94.71    | 97.02  | 95.57 | 96.42    | 95.06 | 92.02   | 95.15  |
| MaskGAE   | 94.82 | 92.78    | 92.79  | 96.93 | 96.57    | 96.69 | 97.15   | 95.39  |
| AFGRL     | 95.29 | 94.69    | 96.54  | 82.75 | 75.99    | 94.81 | 94.52   | 90.66  |
| COSTA     | 88.39 | 86.14    | 94.37  | 79.06 | 82.62    | 88.55 | 87.26   | 86.63  |
| DGI       | 95.48 | 96.75    | 97.37  | 83.97 | 84.91    | 84.57 | 92.79   | 90.83  |
| MVGRL     | 93.33 | 88.66    | 95.89  | 69.58 | 92.37    | 91.45 | 87.92   | 88.46  |
| GRACE     | 80.94 | 83.21    | 97.11  | 85.24 | 83.36    | 87.67 | 84.57   | 86.01  |
| GCA       | 81.46 | 84.81    | 94.2   | 70.02 | 89.92    | 84.35 | 85.75   | 84.36  |
| CCA-SSG   | 95.77 | 94.29    | __98.09__  | 97.97 | 86.6     | 83.34 | 98.6    | 93.52  |
| CAN       | 93.67 | 94.56    | -      | 97    | 96.03    | -     | -       | -      |
| SIG-VAE   | 94.1  | 92.88    | 85.89  | 94.98 | 91.14    | 95.26 | 96.47   | 92.96  |
| GraphMAE  | 93.79 | 94.06    | 92.75  | 70.87 | 67.68    | 95.58 | 95.95   | 87.24  |
| SEEGERA   | 95.97 | 92.31    | 84.88  | __98.02__ | __98.77__    | 97.87 | 97.24   | 95.01  |
| GCLFormer | __96.91__ | __97.53__    | 89.52  | 92.4  | 95.97    | __98.88__ | __99.19__   | __95.77__  |


### Experiments on link prediction, the AP is reported
| AP        | Cora  | CiteSeer | PubMed | Photo | Computer | CS    | Physics | Mean   |
|-----------|-------|----------|--------|-------|----------|-------|---------|--------|
| BGRL      | 92.15 | 90.24    | 94.61  | 92.56 | 95.06    | 91.53 | 89.47   | 92.23  |
| MaskGAE   | 94.22 | 92.15    | 92.71  | 92.74 | 95.37    | 96.8  | 97.18   | 94.45  |
| AFGRL     | 96.34 | 95.77    | 96.28  | 80.87 | 72.98    | 94.97 | 95.32   | 90.36  |
| COSTA     | 79.98 | 87.38    | 93.19  | 78.16 | 82.99    | 90.34 | 91.28   | 86.19  |
| MVGRL     | 92.95 | 89.37    | 95.53  | 63.43 | 91.73    | 89.14 | 86.47   | 86.95  |
| GRACE     | 82.57 | 81.95    | 96.77  | 83.17 | 83.39    | 86.84 | 83.39   | 85.44  |
| GCA       | 80.87 | 81.93    | 93.31  | 65.17 | 89.5     | 83.24 | 82.86   | 82.41  |
| CCA-SSG   | 96.33 | 95.33    | __97.99__  | __97.71__ | 86.97    | 76.31 | 98.57   | 92.74  |
| CAN       | 94.49 | 95.49    | -      | 96.68 | 95.96    | -     | -       | -      |
| SIG-VAE   | 94.79 | 94.21    | 85.02  | 94.53 | 91.23    | 94.93 | 96.28   | 93.00  |
| GraphMAE  | 94.01 | 94.78    | 92.26  | 67.96 | 61.05    | 94.6  | 95.22   | 85.70  |
| SEEGERA   | 96.65 | 93.79    | 83.96  | 97.69 | __98.81__    | 97.12 | 98.12   | 95.16  |
| GCLFormer | __97.14__ | __97.19__    | 89.27  | 90.52 | 95.97    | __98.07__ | __99.4__    | __95.37__  |

In general, Contrastive based methods are more good at node level task and generative based methods excels at link prediction tasks because generative based methods try to reconstruct the topology while contrastive learning focus on the similarity between positive samples. But GCLFormer utalize the attention calculation, so to some extent, we also try to reconstruct the topology, so GCLFormer also performs well on link prediction tasks.