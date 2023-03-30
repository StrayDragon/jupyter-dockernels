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

## Golang

```shell
docker build --tag go-1.20-dockernel -f go-1.20/Dockerfile .
dockernel install go-1.20-dockernel --name go1.20-DK --language go
```

# 其他 Jupyter Kernels :)
- https://gist.github.com/chronitis/682c4e0d9f663e85e3d87e97cd7d1624