# PLMDeepSmart

有关DeepSmart到KNX的配置文件，见HA目录。不同的户型可能需要不同的配置文件

DeepSmart自己的控制逻辑在DeepSmart目录中，供备份

## 简易指南

1. 购买HA盒子
2. 插线接入锐捷的网络
3. 访问HA盒子的IP:8123 （可能需要在交换机APP上找一下具体IP）
4. 添加KNX集成（设置-设备与服务-搜索KNX-添加中枢），会自动扫描到我们的KNX网关
5. 使用文件编辑器(设置-加载项-FileEditor-打开网页界面)选中HA盒子的configuration.yaml，添加一行`knx: !include KNX_S145B.yaml`
6. 新建文件KNX_S145B.yaml，粘贴KNX_S145B_B3.yaml中的内容进去
7. 重载配置（开发者工具-配置检查与重启（检查配置）-重新启动）
8. 首页修改仪表盘，点击右上角原始配置编辑器，粘入HA仪表盘_S145B_B3.yaml内容，保存刷新
