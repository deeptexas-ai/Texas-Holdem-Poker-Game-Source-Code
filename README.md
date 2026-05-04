# Texas Hold'em Game Server|完整德州扑克游戏 / Complete Texas Hold'em poker game / 完整德州撲克遊戲**  
专业规则引擎+流畅UI+实时对战+锦标赛+数据统计，支持单机/联网 / Professional engine+smooth UI+realtime play+tournaments+stats / 專業規則引擎+流暢UI+即時對戰+錦標賽+數據統計

[![License: AGPL v3](https://img.shields.io/badge/License-AGPLv3-blue.svg)](LICENSE)
[![C++17](https://img.shields.io/badge/C%2B%2B-17-blue)](https://isocpp.org/)
[![Docker](https://img.shields.io/badge/docker-ready-brightgreen)](docker-compose.yml)
[![Build Status](https://img.shields.io/github/actions/workflow/status/deeptexas-ai/Texas-Hold-em-game/build.yml?branch=main)]()

**生产级德州扑克服务端** — 已上线App Store/Google Play，支持金币模式、联盟俱乐部、多赛事。

## ✨ 核心特性

| 模块 | 支持内容 |
|------|----------|
| 🎮 **游戏玩法** | 经典德州、短牌、SNG、MTT、竞技场 |
| 🏆 **联盟系统** | 多俱乐部数据互通，排行榜与分红 |
| 📱 **全平台** | 可编译为iOS/Android App (Unity/C#前端) |
| 🗣️ **语音聊天** | 内置实时语音，朋友局专用 |
| ⚡ **高性能** | C++17 + Redis，单服支撑500+桌 |
| 🔐 **公平随机** | 密码学安全随机数，对局可审计 |
### **🎯 游戏模式**
| 模式 | 玩家 | 特色 |
|------|------|------|
| **练习模式** | 2-9人 | 暂停分析，盲注自定义 |
| **锦标赛** | 9人淘汰 | 盲注递增，实时排行 |
| **快速对战** | 6人 | 固定规则，快速开局 |
| **观战模式** | 无限 | 学习高手对局 |
## 📸 联系：
📱 Telegram: @xuzongbin001

📧 Email: masterai918@gmail.com



## 📸 界面截图
![大厅01](Screenshots/大厅01.png)  
**金币大厅界面 | Gold Coin Lobby**

![大满贯](Screenshots/大满贯.jpg)  
**大满贯界面 | Grand Slam**

![大转盘01](Screenshots/大转盘01 (1).jpg)  
**大转盘活动界面 | Lucky Wheel**

![多座竞标赛1](Screenshots/多座竞标赛1.jpg)  
**多桌锦标赛界面 | Multi-Table Tournament**

![保险3](Screenshots/保险3.jpg)  
**保险功能界面 | Insurance**

![新手训练营](Screenshots/新手训练营.png)  
**新手训练营界面 | Beginner Training**

![SNG05](Screenshots/sng05.jpg)  
**SNG竞赛界面 | Sit & Go**

![04](Screenshots/04.png)  
**游戏界面示例 | Gameplay Example**




## 🚀 快速开始（三种方式）

### 方式一：Docker 一键运行（推荐）

git clone https://github.com/deeptexas-ai/Texas-Hold-em-game.git
cd Texas-Hold-em-game
docker-compose up -d
# 服务地址：http://localhost:8080
方式二：源码编译（Ubuntu 20.04）
# 1. 安装依赖
sudo apt-get update
sudo apt-get install -y cmake g++ libboost-all-dev libssl-dev libmysqlcppconn-dev redis-server mysql-server

# 2. 编译
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)

# 3. 初始化数据库
mysql -u root -p < ../scripts/init_db.sql

# 4. 启动服务
./poker_server --config ../config/server.ini
🏗️ 系统架构
Unity客户端 ↔ WebSocket ↔ Nginx网关 ↔ 游戏服务(C++) ↔ Redis(状态) ↔ MySQL(数据)

##  📖 完整文档
文档	说明
部署指南	生产环境（K8s/裸机/云原生）
API协议	WebSocket消息格式与示例
客户端接入	Unity/iOS/Android SDK集成
玩法配置	盲注、抽水、赛事模板
运维手册	监控告警、数据备份、扩容
📊 性能基准
单服并发牌桌：500+ (实测c5.2xlarge)

平均延迟：< 30ms (P99)

系统可用性：99.99%

单服内存：< 4GB (2000人负载)

## 🤝 商业支持
本项目为AGPL开源，免费使用。如需商业授权（去GPL限制）、定制开发、运维托管：





## 📜 开源协议
Copyright © 2025 deeptexas-ai

GNU Affero General Public License v3.0

## ⭐ 支持项目
如果这个项目对你有帮助，请点亮右上角的 Star，这是对我们最大的鼓励！


## 🛠️ 版本发布 / Releases / 版本發佈

### 🚀 v1.0.0 (稳定版)
✅ 完整德州规则  
✅ 多模式锦标赛  
✅ 数据统计系统  
✅ 6套主题  
✅ 全平台支持  


