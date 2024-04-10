## Experiments on more baselines

We add BGRL, MASKGAE, AFGRL and COSTA as baseline and report their performance. Also, we train the previous "OOM" result in batched manner to show the performance.

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
| BRGL      | 84.27 | 73.04    | 84.47  | 92.89 | 89.72    | 93.97 | 95.64   | 87.71  |
| MaskGAE   | 84.52 | __73.32__    | 85.26  | 92.74 | 89.41    | 93.46 | 95.82   | 87.79  |
| AFGRL     | 84.46 | 72.45    | 84.92  | 93.14 | __89.74__    | 93.16 | 95.32   | 87.60  |
| COSTA     | 84.73 | 72.05    | 84.31  | 92.17 | 88.41    | 92.73 | 95.41   | 87.12  |
| GRACE     | 84.08 | 71.76    | 86.03  | 77.79 | 77.98    | 89.65 | 94.82   | 83.16  |
| DGI       | 83.86 | 70.25    | 86.05  | 92.21 | 88.03    | 90.36 | 94.71   | 86.50  |
| CCA-SSG   | 83.71 | 70.45    | __86.07__  | 92.76 | 79.26    | 93.18 | 95.7    | 85.88  |
| MVGRL     | 83.5  | 72.3     | 80.1   | 91.74 | 87.52    | 92.11 | 95.28   | 86.08  |
| GraphMAE  | 84.46 | 72.81    | 85.8   | 88.81 | 81.87    | 92.69 | 95.53   | 86.00  |
| SeeGera   | 84.34 | 71.72    | 85.68  | 92.33 | 88.27    | 93.79 | 95.79   | 87.42  |
| GCLFormer | __84.74__ | 72.97    | 85.32  | __93.71__ | 87.47    | __94.87__ | __95.98__   | __87.87__  |



### Experiments on link prediction, the ROC is reported

The result of CAN is omited because CAN takes the feature of nodes as sparse matrix with only "0" and "1", so it fails on some datasets like PubMed.

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

The result of CAN is omited because CAN takes the feature of nodes as sparse matrix with only "0" and "1", so it fails on some datasets like PubMed.

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