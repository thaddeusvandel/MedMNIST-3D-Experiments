# MedMNIST 3D Experiments

Replication of 3D ResNet-50 experiments on all 6 MedMNIST3D datasets as part of a pre-warm-up exercise for AI research in medical imaging.

## Datasets
Trained and evaluated on all 6 MedMNIST3D datasets from the
[MedMNIST v2 benchmark](https://medmnist.com/), including OrganMNIST3D,
NoduleMNIST3D, AdrenalMNIST3D, FractureMNIST3D, VesselMNIST3D, and SynapseMNIST3D.

## Model
- Architecture: ResNet-50 + 3D
- Each dataset trained 5 times
- Metrics: AUC and Accuracy

## Results
| Dataset           | AUC (mean ± std) | ACC (mean ± std) |
|-------------------|------------------|------------------|
| OrganMNIST3D      |0.9939 ± 0.0030   |0.9168 ± 0.0023   |
| NoduleMNIST3D     |0.8609 ± 0.0099   |0.8455 ± 0.0058   |
| AdrenalMNIST3D    |0.8443 ± 0.0022   |0.8092 ± 0.0058   |
| FractureMNIST3D   |0.6129 ± 0.0081   |0.4755 ± 0.0060   |
| VesselMNIST3D     |0.8883 ± 0.0114   |0.9320 ± 0.0076   |
| SynapseMNIST3D    |0.6947 ± 0.0181   |0.7585 ± 0.0095   |

## Setup
```bash
pip install -r requirements.txt
python train.py --dataset organmnist3d
```

## References
- MedMNIST v2: https://doi.org/10.1038/s41597-022-01721-8
- Original experiments: https://github.com/MedMNIST/experiments