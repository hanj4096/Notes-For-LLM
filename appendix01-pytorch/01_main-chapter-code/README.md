# 附录A：PyTorch简介

### 主要章节代码

- [code-part1.ipynb](code-part1.ipynb) 包含章节中出现的所有A.1到A.8节的代码
- [code-part2.ipynb](code-part2.ipynb) 包含章节中出现的所有A.9节GPU代码
- [DDP-script.py](DDP-script.py) 包含演示多GPU使用的脚本（注意Jupyter Notebooks仅支持单GPU，所以这是一个脚本，而不是notebook）。您可以通过 `python DDP-script.py` 运行它。如果您的机器有超过2个GPU，可以通过 `CUDA_VISIBLE_DEVIVES=0,1 python DDP-script.py` 运行它。
- [exercise-solutions.ipynb](exercise-solutions.ipynb) 包含本章的练习解决方案

### 可选代码

- [DDP-script-torchrun.py](DDP-script-torchrun.py) 是 `DDP-script.py` 脚本的可选版本，它通过PyTorch的 `torchrun` 命令运行，而不是通过 `multiprocessing.spawn` 自己生成和管理多个进程。`torchrun` 命令的优势是自动处理分布式初始化，包括多节点协调，这稍微简化了设置过程。您可以通过 `torchrun --nproc_per_node=2 DDP-script-torchrun.py` 使用此脚本
