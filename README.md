# Resource-Aware Neural Architecture Adaptation

This project explores how a neural network can adapt its computation based on available hardware resources. Instead of always running the full model, the system decides how deep to go based on what the device can handle and how confident the model already is.
We use a Vision Transformer trained on CIFAR-10 with two early exit points. A decision controller checks confidence and resource availability at each exit point and decides whether to stop or keep going. The system is tested across three real hardware setups: a 6GB GPU, a 4GB GPU, and a CPU-only machine.
On top of the base system, we introduce two new ideas. The first is resource drift monitoring, where instead of checking hardware load once per inference, the system tracks whether load is increasing over time and reacts before performance drops. The second is confidence drift detection, where instead of only checking the current confidence score, the system watches how confidence changes across exit points and exits early if deeper layers are not actually improving the prediction.
The goal is to show that a single model can run efficiently across very different hardware by being smart about when to stop computing.

## Tech stack:

Language: Python 3.10+

Deep Learning: PyTorch, timm

Resource Monitoring: pynvml, psutil, torch.cuda

Data: torchvision

Analysis: pandas, matplotlib, scikit-learn

Environment: Conda

Dev Tools: VS Code, Git, GitHub

RL (future)

## To clone the repository:

git clone https://github.com/BSaiCharan-GH/resource-aware-ai.git
Enter the project folder: cd resource-aware-ai


## Use this command on CMD or VScode terminal to install requirements:

pip install -r requirements.txt


