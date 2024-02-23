1. 本nginx 配置专为 xiao ya emby 项目定制，不适用于其他项目
2. 主要解决以下问题
   1. 代理请求到后端服务
   2. 拦截 emby 请求，重定向到 xiaoya docker ，返回直链给客户端，避免 emby 服务端拉流
   3. 在剧集页面注入 js 方便调用外部播放器

3. 使用方法：
   1. 修改`docker-compose.yml`中的环境变量
   2. 执行`chmod +x nginx/entry.sh`赋予启动脚本可执行权限
   3. 执行`docker-compose up -d`启动服务
   4. `docker logs nginx -f` 查看日志
