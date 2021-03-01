# jenkins

https://www.jenkins.io/


## 安装

### windows
1. https://www.jenkins.io/download/thank-you-downloading-windows-installer-stable/
2. 问题
  - this account either does not have the privilege logon as a service
    - https://blog.csdn.net/Chenftli/article/details/108487494
      - 控制面板 管理工具 本地安全策略 本地策略 用户权限分配 作为服务登录
        - 添加用户或组 输入windows账号 检查名称 确定
3. 安装完自动打开
  - http://localhost:8080/login?from=%2F
4. 解锁 Jenkins
  - C:\Users\[xxxx]\AppData\Local\Jenkins\.jenkins\secrets\initialAdminPassword
  - loading 等待
5. 安装插件
  - 先选择默认插件
  - 等待
  - 部分插件失败
  - 先下一步
    - Manage Jenkins
      - Manage Plugins
        - 高级
          - 升级站点
            - 修改 URL 为 http://mirror.esuni.jp/jenkins/updates/update-center.json
              - 点当没有任务时重启
