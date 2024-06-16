## 1 运行api接口程序

- **REPO_OWNER**：  仓库空间名称
- **REPO_NAME**：     仓库项目名称
- **GITHUB_TOKEN**：GitHub 个人token密钥
- **BRANCH_NAME**：分支

```bash
docker run -d --name github-flask-api \
	-p 8088:80 \
    -e REPO_OWNER="iCloudBot" \
    -e REPO_NAME="DockerRescue" \
    -e GITHUB_TOKEN="ghp_***********************" \
    -e BRANCH_NAME="main" \
    registry.cn-chengdu.aliyuncs.com/dockerip/github-flask-api
```

```yaml
# 或者
cat > docker-compose.yml <<EOF
services:
  adguardhome:
    image: registry.cn-chengdu.aliyuncs.com/dockerip/github-flask-api
    container_name: github-flask-api
    restart: unless-stopped
    ports:
      - 8088:80
    environment:
      REPO_OWNER: iCloudBot
      REPO_NAME: DockerRescue
      BRANCH_NAME: main
      GITHUB_TOKEN: ghp_***********************
EOF

docker comopse up -d
```

## 2 测试接口请求

```bash
curl http://localhost:8088/images?image_names=nginx,alpine:latest,adguard/adguardhome

curl http://localhost:8088/images?image_names=nginx,alpine:latest,adguard/adguardhome&arch=arm/v7

curl http://localhost:8088/images?image_names=nginx,alpine:latest,adguard/adguardhome&arch=arm/v7&email=cleverest@qq.com
```

