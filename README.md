# gitea-docker-compose

## 配置信息

### 安装

```bash
git clone https://github.com/yaimeet/gitea-docker-compose.git

cd  gitea-docker-compose
```

### 创建环境变量文件

```bash
cp .env.simaple .env
```

### 修改环境变量

```bash
vim .env
```

- GITEA_WEB_PORT # web访问的端口
- GITEA_SSH_PORT # ssh 链接访问的端口
- GITEA_SERVER # 一般为：http://IP:web访问的端口


### 使用

```bash
docker-compose up -d   # 启动
docker-compose down   # 卸载
docker-compose restart   # 重启 修改了 gitea 配置信息时需要重启
```

### gitea 配置

启动之后，数据卷默认全部挂载在当前目录下的 `data` 目录中。

```bash
vim ./data/gitea/gitea/conf/app.ini
```