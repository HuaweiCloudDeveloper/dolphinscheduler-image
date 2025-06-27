# DolphinScheduler工作流任务调度平台使用指南

# 一、商品链接

[DolphinScheduler工作流任务调度平台](https://marketplace.huaweicloud.com/hidden/contents/31496fe8-a3c9-402a-863f-4b786940a410#productid=OFFI1121281616205033472)

# 二、商品说明

**Apache DolphinScheduler** 是一个分布式和可扩展的开源工作流协调平台，具有强大的DAG可视化界面，致力于解决数据管道中复杂的任务依赖关系，并提供“开箱即用”的各种类型的作业。

# 三、商品购买

您可以在云商店搜索 **DolphinScheduler工作流任务调度平台**。

其中，地域、规格、推荐配置使用默认，购买方式根据您的需求选择按需/按月/按年，短期使用推荐按需，长期使用推荐按月/按年，确认配置后点击“立即购买”。


## 3.1 使用 RFS 模板直接部署
![img.png](images/img1.png)
必填项填写后，点击 下一步
![img.png](images/img2.png)
![img.png](images/img3.png)
创建直接计划后，点击 确定
![img.png](images/img4.png)
![img.png](images/img5.png)
点击部署，执行计划
![img.png](images/img6.png)
如下图“Apply required resource success. ”即为资源创建完成
![img.png](images/img7.png)
# 3.2 ECS 控制台配置

### 准备工作

在使用ECS控制台配置前，需要您提前配置好 **安全组规则**。

> **安全组规则的配置如下：**
> - 入方向规则放通端口12345，源地址内必须包含您的客户端ip，否则无法访问
> - 入方向规则放通 CloudShell 连接实例使用的端口 `22`，以便在控制台登录调试
> - 出方向规则一键放通

### 创建ECS

前提工作准备好后，选择 ECS 控制台配置跳转到[购买ECS](https://support.huaweicloud.com/qs-ecs/ecs_01_0103.html) 页面，ECS 资源的配置如下图所示：

选择CPU架构
![img.png](images/img8.png)
选择服务器规格
![img_1.png](images/img_1.png)
选择镜像
![img_2.png](images/img_2.png)
其他参数根据实际请客进行填写，填写完成之后，点击立即购买即可
![img_3.png](images/img_3.png)


> **值得注意的是：**
> - VPC 您可以自行创建
> - 安全组选择 [**准备工作**](#准备工作) 中配置的安全组；
> - 弹性公网IP选择现在购买，推荐选择“按流量计费”，带宽大小可设置为5Mbit/s；
> - 高级配置需要在高级选项支持注入自定义数据，所以登录凭证不能选择“密码”，选择创建后设置；
> - 其余默认或按规则填写即可。

# 商品使用

## 启动dolphinscheduler服务 (单机版)
-- apache-dolphinscheduler源文件存放路径

cd /opt/soft/dolphinscheduler/apache-dolphinscheduler-3.1.4-bin

```bash
# 启动 Standalone Server 服务
bash ./bin/dolphinscheduler-daemon.sh start standalone-server

# 停止 Standalone Server 服务
bash ./bin/dolphinscheduler-daemon.sh stop standalone-server

# 查看 Standalone Server 状态
bash ./bin/dolphinscheduler-daemon.sh status standalone-server
```

### 其它 启动/停止 服务命令参考
```bash
# 一键停止集群所有服务
sh /opt/soft/dolphinscheduler-3.1.4/bin/stop-all.sh

# 一键启动集群所有服务
sh /opt/soft/dolphinscheduler-3.1.4/bin/start-all.sh

# 启/停 master 服务
sh /opt/soft/dolphinscheduler-3.1.4/bin/dolphinscheduler-daemon.sh start master-server
sh /opt/soft/dolphinscheduler-3.1.4/bin/dolphinscheduler-daemon.sh stop master-server

# 启/停 worker 服务
sh /opt/soft/dolphinscheduler-3.1.4/bin/dolphinscheduler-daemon.sh start worker-server
sh /opt/soft/dolphinscheduler-3.1.4/bin/dolphinscheduler-daemon.sh stop worker-server

# 启/停 api 服务
sh /opt/soft/dolphinscheduler-3.1.4/bin/dolphinscheduler-daemon.sh start api-server
sh /opt/soft/dolphinscheduler-3.1.4/bin/dolphinscheduler-daemon.sh stop api-server

# 启/停 alert 服务
sh /opt/soft/dolphinscheduler-3.1.4/bin/dolphinscheduler-daemon.sh start alert-server
sh /opt/soft/dolphinscheduler-3.1.4/bin/dolphinscheduler-daemon.sh stop alert-server
```
### 访问 web 页面
http://ip:12345/dolphinscheduler/ui/home 

-- ip 需要改成自己的公网 ip  默认的登录用户/密码：admin/dolphinscheduler123

### 参考文档

[dolphinscheduler官网](https://dolphinscheduler.apache.org/zh-cn)
