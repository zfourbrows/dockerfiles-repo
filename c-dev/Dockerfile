# 使用 Ubuntu 22.04 作为基础镜像
FROM ubuntu:22.04

# 设置工作目录（进入容器后默认在这个目录）
WORKDIR /workspace

# C语言开发环境：更新软件源并安装 Git、Vim 等工具
# gcc-编译套件、make-管理多文件编译、gdb-调试程序，debug
RUN apt update && \
    apt install -y \
    git \
    vim \
    gcc \
    make \
    gdb \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

# 设置终端提示符（可选，让界面更清晰）
ENV PS1="\u@\h:\w\$ "

# 容器启动时默认进入 /workspace 并打开 bash
CMD ["/bin/bash"]