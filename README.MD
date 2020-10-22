Mac OS下连接docker容器网络

1. ```shell
   brew install jq
   ```

2. ```shell
   cd ~/Library/Group\ Containers/group.com.docker/
   mv settings.json settings.json.backup
   cat settings.json.backup | jq '.["socksProxyPort"]=8888' > settings.json
   ```

3. 重启Docker

4. 系统偏好设置 -> 网络 -> 高级 -> 代理 -> 自动代理配置

   - 代理配置文件 URL `https://raw.githubusercontent.com/hcolde/docker-proxy/main/docker.pac`

