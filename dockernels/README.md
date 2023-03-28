# 安装

确保已经安装好 dockernel

## 务必执行
```shell
cd dockernels
```

## Rust

```shell
docker build --tag rust-1.68-dockernel -f rust-1.68/Dockerfile .
dockernel install rust-1.68-dockernel --name rust1.68-DK --language rust
```

## Python

```shell
docker build --tag python-3.11-dockernel -f python-3.11/Dockerfile .
dockernel install python-3.11-dockernel --name py3.11-DK --language python
```