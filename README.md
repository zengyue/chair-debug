# chair-debug
Visual Studio Code plugin for chair

# Getting Started

1. 添加`launch.json`, 可以通过`debug`菜单项直接添加
2. 添加debug配置，配置文件如下
````
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "attach",
      "name": "Attach to Process",
      "processId": "${command:extension.pickChairProcess}",
      "port": 5858,
      "restart": true
    }
  ]
}
````

这里主要关注`processId`这个配置项，`restart`配置当修改文件，app worker 重启后，是否自动`attach` worker 进程
