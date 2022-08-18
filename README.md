```bash
curl -fsSL https://github.com/mikucloud/v2/raw/master/install.sh | bash -s API TOKEN NODEID LICENSE 60
```

```bash
docker run -d --name=aurora \
-v /root/.cert:/root/.cert \
-e API=API \
-e TOKEN=TOKEN \
-e NODE=NODEID \
-e LICENSE=LICENSE \
-e SYNCINTERVAL=60 \
--restart=always \
--network=host \
mikucloud/aurora
```

## 申请TLS证书

1.首先将节点域名解析到节点服务器，并且可以ping通

```bash
curl -fsSL https://github.com/mikucloud/v2/raw/master/sign.sh | bash -s domain.com
```

2.申请完成后证书将会保存至/root/.cert/server.crt /root/.cert/server.key
