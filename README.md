# SARD: Structure-Aware Representation Distillation for Tiny-Dense Object Segmentation

**CVPR 2026**

> Xuesong Liu, Anke Xu, Wenbo Cao, Emmett Ientilucci

## Installation

```bash
git clone https://github.com/liuuuuuuxuesong/SARD.git
cd SARD
pip install -r requirements.txt
```

## Data Preparation

Download and organize datasets under `data/`:

- [Cityscapes](https://www.cityscapes-dataset.com/)
- [ADE20K](http://sceneparsing.csail.mit.edu/)
- RockFrag

## Usage

### Train

```bash
python train.py --config configs/sard_swinl_swint_cityscapes.yaml
```

### Evaluate

```bash
python eval.py --config configs/sard_swinl_swint_cityscapes.yaml --ckpt /path/to/checkpoint.pth
```

## Project Structure

```
SARD/
├── configs/              # Training configs
├── sard/
│   ├── models/           # Teacher & student architectures
│   ├── losses/           # L_FC, L_DA, Dice+BCE
│   └── structure/        # Structure tensor, E(i), C(i), D(i), W(i)
├── train.py
├── eval.py
└── requirements.txt
```

## License

MIT
