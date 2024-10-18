# fugaku-llm-chatbot
This project is destined to understand a simple model used at the ChatBot. The ChatBot created here will be like GPT-2.

## Prerequisites

- Docker

I have tested with an environment below.

- WSL 2

- GeForce RTX 2070 (8GB RAM)

- AMD Ryzen 7 3700X

- 16GB RAM

## Getting Started
Start a container.

    ./run.sh

Run in the container.

    pip install transformers accelerate --use-feature=2020-resolver
    huggingface-cli login
    python3 main.py

output:

    root@4d5f84a5e6d8:/workspace# time python3 main.py
    /opt/conda/lib/python3.8/site-packages/huggingface_hub/file_download.py:1132: FutureWarning: `resume_download` is deprecated and will be removed in version 1.0.0. Downloads always resume when possible. If you want to force a new download, use `force_download=True`.
    warnings.warn(
    Loading checkpoint shards: 100%|█████████████████████████████████████| 6/6 [00:01<00:00,  4.43it/s]
    /opt/conda/lib/python3.8/site-packages/huggingface_hub/file_download.py:1132: FutureWarning: `resume_download` is deprecated and will be removed in version 1.0.0. Downloads always resume when possible. If you want to force a new download, use `force_download=True`.
    warnings.warn(
    WARNING:root:Some parameters are on the meta device device because they were offloaded to the cpu and disk.
    以下は、タスクを説明する指示です。要求を適切に満たす応答を書きなさい。

    ### 指示:
    スーパーコンピュータ「富岳」の名前の由来を教えてください。

    ### 応答:
    「富岳」は日本の理化学研究所と富士通が共同で開発したスーパーコンピュータで、富士山の異名である「富嶽」に由来している。この名前は、スーパーコンピュータが日本の研究コミュニティや産業界に広く受け入れられ、広く使用されることを願って付けられた。また、富士山が高く評価され、愛されている日本の象徴であることから、この名前が選ばれた。

    real    25m35.436s
    user    4m53.496s
    sys     4m50.370s

## References:

1. [Fugaku LLM ChatBot][1]
2. [Fugaku-LLM DeepSpeedFugaku][2]
3. [Pytorch Nvidia][3]
4. [Awesome Japanese LLM][4]
5. [Nvidia Driver Download][5]
6. [Nvidia Container Toolkit][6]
7. [Nvidia Container Toolkit Documentation][7]
8. [Ollama Instructions to Use Fugaku-LLM 13B GGUF][8]
9. [Ollama Instructions to Use Fugaku-LLM 13B GGUF by Ubuntu][9]
10. [Fugaku LLM ChatBot How to Build][10]
11. [Fugaku LLM ChatBot How to Build 2][11]
12. [Fugaku LLM ChatBot Ollama Chat Interface][12]

[1]: https://huggingface.co/Fugaku-LLM/Fugaku-LLM-13B-instruct
[2]: https://github.com/Fugaku-LLM/DeepSpeedFugaku
[3]: https://catalog.ngc.nvidia.com/orgs/nvidia/containers/pytorch
[4]: https://github.com/llm-jp/awesome-japanese-llm
[5]: https://www.nvidia.com/content/DriverDownloads/confirmation.php?url=/Windows/531.61/531.61-desktop-win10-win11-64bit-international-dch-whql.exe&lang=us&type=GeForce
[6]: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/1.14.4/release-notes.html
[7]: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/1.14.4/index.html
[8]: https://zenn.dev/hellorusk/articles/94bf32ea09ba26
[9]: https://tech.takuyakobayashi.jp/2024/05/18/23
[10]: https://note.com/owlet_notes/n/nd144bd2d1dc1
[11]: https://note.com/ngc_shj/n/n7a8ce01f13ac
[12]: https://github.com/ollama-ui/ollama-ui
