<p align="center">
  <h1 align="center">DolphinScheduler Workflow Task Scheduling Platform</h1>
  <p align="center">
    <a href="README_ZH.md"><strong>简体中文</strong></a> | <strong>English</strong>
  </p>

## Table of Contents

- [Repository Introduction](#repository-introduction)  
- [Prerequisites](#prerequisites)  
- [Image Specifications](#image-specifications)
- [Getting Help](#getting-help)
- [How to Contribute](#how-to-contribute)

## Repository Introduction  
[Apache dolphinscheduler](https://github.com/apache/dolphinscheduler) is the modern data orchestration platform. Agile to create high performance workflow with low-code.

**Core Features:**
1. By using a DAG graph to associate tasks based on their dependencies, real-time visualization of the task's operational status can be achieved.  
2. Rich types of tasks available: Shell、MR、Spark、SQL(mysql、postgresql、hive、sparksql),Python,Sub_Process、Procedure、Flink  And HTTP tasks, etc.  
3. Implement cluster HA and decentralize Master and Worker clusters through Zookeeper.  
4. Support workflow scheduled scheduling, dependency scheduling, manual scheduling, manual pause/stop/resume, while also supporting failed retry/alarm, failed recovery from designated nodes, Kill tasks, and other operations.  

**Architecture Design:**

![](./images/img01.png)

This project offers pre-configured [**Apache dolphinscheduler**](https://marketplace.huaweicloud.com/intl/hidden/contents/9f9bc006-7f3b-4038-8a12-3c271bbbfdb4) images with DolphinScheduler and its runtime environment pre-installed, along with deployment templates. Follow the guide to enjoy an "out-of-the-box" experience.

> **System Requirements:**
> - CPU: 2GHz or higher  
> - RAM: 4GB or more  
> - Disk: At least 40GB  

## Prerequisites  
[Register a Huawei account and activate Huawei Cloud](https://support.huaweicloud.com/usermanual-account/account_id_001.html)

## Image Specifications  

| Image Version                                                                                                                        | Description                                                    | Notes |  
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-------|  
| [dolphinscheduler3.1_HCE2.0](https://marketplace.huaweicloud.com/intl/hidden/contents/9f9bc006-7f3b-4038-8a12-3c271bbbfdb4)          | Deployed on Kunpeng servers with Huawei Cloud EulerOS 2.0 64bit |  | 
| [dolphinscheduler3.1_Ubuntu24.04](https://marketplace.huaweicloud.com/intl/hidden/contents/9f9bc006-7f3b-4038-8a12-3c271bbbfdb4)     | Deployed on Kunpeng servers with Ubuntu24.04 64bit        |  |  
| [DolphinScheduler3.2.2-x86-v1.0](https://github.com/HuaweiCloudDeveloper/dolphinscheduler-image/tree/DolphinScheduler3.2.2-x86-v1.0) | Deployed on X86 servers with CentOS 7.6 64bit            |  |  

## Getting Help
- Submit an [issue](https://github.com/HuaweiCloudDeveloper/dolphinscheduler-image/issues)
- Contact Huawei Cloud Marketplace product support

## How to Contribute
- Fork this repository and submit a merge request.
- Update README.md synchronously based on your open-source mirror information.
