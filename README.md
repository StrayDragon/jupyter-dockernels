# Jupyter dockernels
[![pdm-managed](https://img.shields.io/badge/pdm-managed-blueviolet)](https://pdm.fming.dev)
![platform](https://img.shields.io/badge/platform-osx-lightgrey)

使用 [dockernel](https://github.com/MrMino/dockernel) 管理更多 jupyter 支持的内核 (jupyter kernels), 隔离用户环境配置, 临时环境用完即弃!

## 功能一览

> **NOTE**: 查看 [dockernels/](./dockernels/) 获得更多信息
![image](https://user-images.githubusercontent.com/26061593/228177466-8205b78f-2f2c-4798-a50d-1590b4163d04.png)

- 使用 Rust 1.68 (dockernel) 模式写笔记代码
![image](https://user-images.githubusercontent.com/26061593/228176798-08cac8c3-7f68-4e0c-a1ca-e511e71c2484.png)

![image](https://user-images.githubusercontent.com/26061593/228175856-1477e18e-f815-4a01-adeb-e0f381736608.png)


## 依赖

- python3
  - [pdm](https://github.com/pdm-project/pdm)
- Docker

## 安装


### 仅 dockernels
- 你可以仅使用该项目提供的 [dockernels/](./dockernels/)
```
pipx install git+https://github.com/StrayDragon/dockernel@master # for MacOS user
# 或
pipx install dockernel # for other
```
- 然后按照 [dockernels/](./dockernels/) 提供的安装命令安装

### JupyterLab

- 运行一下命令

```shell
pdm install

<see ./dockernels README and run cmds>

pdm run jupyter-lab
# or
. .venv/bin/activate
jupyter-lab
```