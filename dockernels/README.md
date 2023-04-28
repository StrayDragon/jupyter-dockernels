# 安装

确保已经安装好 dockernel

## 首先执行
```shell
cd dockernels
```

## 构建镜像
```shell
docker build --tag <LANG_NAME-LANG_VERSION-DK-KERNEL_NAME> -f <LANG_DOCKERNEL_DOCKERFILE_DIR>/Dockerfile .
dockernel install --name <LANG_NAME-LANG_VERSION-DK-KERNEL_NAME> --language <LANG_TYPE>
```

### 示例

#### Rust

##### evcxr

```shell
docker build --tag rust-1.69-dk-evcxr -f rust/1.69/evcxr/Dockerfile .
dockernel install --name rust-1.69-dk-evcxr --language rust
```

##### irust

```shell
docker build --tag rust-1.69-dk-irust -f rust/1.69/irust/Dockerfile .
dockernel install --name rust-1.69-dk-irust --language rust
```

#### Python

##### ipython
```shell
docker build --tag python-3.11-dk-ipython -f python/3.11/ipython/Dockerfile .
dockernel install --name python-3.11-dk-ipython --language python
```

#### Golang

##### gonb

```shell
docker build --tag go-1.20-dk-gonb -f go/1.20/gonb/Dockerfile .
dockernel install --name go-1.20-dk-gonb --language go
```

##### gophernote (deprecated: not support official generic)
```shell
docker build --tag go-1.20-dk-gophernote -f go/1.20/gophernote/Dockerfile .
dockernel install --name go-1.20-dk-gophernote --language go
```

# 卸载
```shell
dockernel uninstall --name <DOCKERNEL_NAME_OR_IMAGE_NAME>
```

# 查看已安装列表
```shell
dockernel install --list
```

# 其他 Jupyter Kernels :)
- https://gist.github.com/chronitis/682c4e0d9f663e85e3d87e97cd7d1624
