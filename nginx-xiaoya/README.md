1. 本nginx 配置专为 xiao ya emby 项目定制，不适用于其他项目
2. 主要解决以下问题
    - 1. 代理请求到后端服务
    - 2. 拦截emby请求，重定向到aliyun oss，避免emby服务端拉流
    - 3. 在剧集页面注入js方便调用外部播放器

3. 使用方法：
    - 1. 修改docker-compose.yml中的环境变量
    - 2. 执行`chmod +x nginx/entry.sh`赋予启动脚本可执行权限
    - 3. 执行`docker-compose up -d`启动服务