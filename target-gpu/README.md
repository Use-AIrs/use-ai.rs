Since we can target nvptx64-nvidia-cuda in the rustc we just can execute mathe
directly on NVIDIA GPUs. For other GPUs we will use rust-gpu to connect to
the spir-v producer.
Here we translate the concurrent operations of core for the gpu for ether
a spir-v or cuda targets.

Here we make all unsafe operators for the GPUs. Since we want to communicate
directly with a GPU kernel we cant use the std library everywhere. But since Core will be
enough for these operators.