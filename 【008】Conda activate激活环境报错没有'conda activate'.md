

适用于已经完成下列排查：

# 1. 确保 Conda 被正确安装并且可访问

确认 Conda 是否安装正确，并且在你的 shell 中可用。执行以下命令：（需要根据anaconda/miniconda路径修改）

```bash
/root/miniconda3/bin/conda --version
```

得到了版本信息，确定 Conda 已经安装并且可用。

# 2. 检查 shell 环境变量

手动检查 shell 环境变量，确保 conda 命令在 PATH 中：

```bash
echo $PATH | grep '/root/miniconda3/bin'
```

# 3. 强制重新加载 .bashrc 文件

执行以下命令以强制重新加载 .bashrc 文件：

```bash
source ~/.bashrc
```

然而仍然报错

```
root@autodl-container-7071118252-968037de:~/autodl-tmp# conda activate

CommandNotFoundError: Your shell has not been properly configured to use 'conda activate'.
To initialize your shell, run

    $ conda init <SHELL_NAME>

Currently supported shells are:
  - bash
  - fish
  - tcsh
  - xonsh
  - zsh
  - powershell

See 'conda init --help' for more information and options.

IMPORTANT: You may need to close and restart your shell after running 'conda init'.
```

此时可以尝试解决方案：

```
source activate
conda deactivate
```

随后即可正常使用

```
conda activate
```
