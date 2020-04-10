# elasticsearch安装步骤
# 步骤1
将下载的elasticsearch解压到指定目录
# 步骤2
运行bin目录下的elasticsearch.bat文件
# 步骤3
访问http://localhost:9200/查看是否安装成功
# 步骤4 安装可视化工具
下载elasticsearch-head
# 步骤5 安装grunt客户端, 需安装node.js
npm install -g grunt -cli
# 步骤6 安装elasticsearch-head依赖
在elasticsearch-head安装目录执行npm install
# 步骤7 查看elasticsearch-head安装是否成功
执行grunt server启动elasticsearch-head, 访问http://localhost:9100/是否正常
# 步骤8 修改elasticsearch配置文件
修改elasticsearch配置文件config/elasticsearch.yml,在底部追加
http.cors.enabled: true
http.cors.allow-origin: "*"
node.master: true
node.data: true
并打开http.port: 9200, node.name: node-1和cluster.name: my-application的注释, 重新启动elasticsearch
# 步骤9
在elasticsearch-head的可视化界面连接elastisearch服务, 查看是否正常

