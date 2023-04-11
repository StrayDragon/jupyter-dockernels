# 安装

确保已经安装好 dockernel

## 务必执行
```shell
cd dockernels
```

## Rust

```shell
# dockernel uninstall --name rust1.68-DK
docker build --tag rust-1.68-dockernel -f rust-1.68/Dockerfile .
dockernel install --image-name rust-1.68-dockernel --name rust1.68-DK --language rust
```

## Python

```shell
# dockernel uninstall --name py3.11-DK
docker build --tag python-3.11-dockernel -f python-3.11/Dockerfile .
dockernel install --image-name python-3.11-dockernel --name py3.11-DK --language python
```

## Golang

### gonb

```shell
# dockernel uninstall --name go1.20-DK-gonb
docker build --tag go-1.20-dockernel-gonb -f go-1.20/gonb/Dockerfile .
dockernel install --image-name go-1.20-dockernel-gonb --name go1.20-DK-gonb --language go
```

### gophernote (deprecated: not support official generic)

```shell
# dockernel uninstall --name go1.20-DK-gophernote
docker build --tag go-1.20-dockernel-gophernote -f go-1.20/gophernote/Dockerfile .
dockernel install --image-name go-1.20-dockernel-gophernote --name go1.20-DK-gophernote --language go
```

# 其他 Jupyter Kernels :)
- https://gist.github.com/chronitis/682c4e0d9f663e85e3d87e97cd7d1624