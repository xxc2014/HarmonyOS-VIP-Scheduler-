⏰ 如时 - 智能订阅续费管家
智能订阅续费管理应用，鸿蒙全场景体验
快速开始 • 功能特性 • 创新亮点 • 技术栈 • 贡献指南
📌 项目简介
如时（原续费管家）是一款专为HarmonyOS生态打造的智能订阅续费管理应用。帮助用户一站式管理所有订阅服务，提供到期智能提醒、账单统计分析、跨设备同步等功能。深度融合鸿蒙分布式能力，实现手机、平板、智能手表等多设备间的无缝协同，让订阅管理变得简单高效。
💡 产品口号：订阅再多，如时掌握
✨ 核心功能特性
📋 订阅管理
一站式管理：支持流媒体、软件、会员、云服务等各类订阅
自定义分类：娱乐、工具、学习、生活等多维度分类
标签系统：灵活打标签，智能过滤筛选
批量操作：批量编辑、批量删除、批量分类
🔔 到期提醒
多级提醒：提前3天、1天、当天多级提醒
智能通知：服务卡片、通知栏、手表多渠道提醒
自定义提醒：为每个订阅设置独立提醒规则
延迟提醒：一键延后，临时取消订阅
一键续费：直接跳转官方续费页面
📥 一键导入
短信智能识别：自动识别续费短信，一键添加
邮箱账单导入：支持邮箱账单自动解析
截图OCR识别：截图自动识别订阅信息
模板导入：支持Excel/CSV批量导入
📊 账单统计
月度支出概览：当月、季度、年度支出统计
分类支出分析：各分类订阅占比饼图
订阅趋势图：支出趋势可视化展示
预算管理：设定订阅预算，超支预警
导出报表：支持PDF/Excel报表导出
🔄 跨设备同步
分布式同步：手机、平板、手表数据实时同步
超级终端：多设备无缝接续操作
原子化服务：手表端快速查看续费提醒
一碰传：设备间快速分享订阅列表
🔒 隐私安全
本地加密存储：所有数据本地加密，不上传云端
无网络也能用：核心功能完全离线可用
生物认证：人脸/指纹保护敏感数据
开源透明：完全开源，代码可审计
🎯 创新亮点
🔥 鸿蒙分布式能力
超级终端协同：手机添加订阅，手表接收提醒
分布式数据管理：基于HarmonyOS分布式数据库
任务流转：在平板上编辑，手机上查看
多设备状态同步：一处修改，多端实时更新
⚡ 原子化服务卡片
多种尺寸：1x2、2x2、2x4服务卡片
动态数据：实时显示即将到期订阅
交互卡片：卡片内直接延期、标记已续费
智能推荐：根据使用习惯推荐展示内容
负一屏集成：智能聚合订阅日历
🛡️ 隐私本地存储
端侧优先：所有数据存储在本地设备
AES-256加密：银行级加密算法
零云依赖：无需注册账号即可使用
开源审计：代码完全开源，隐私有保障
数据导出：支持完整数据备份导出
🎨 鸿蒙设计语言
极简设计：遵循HarmonyOS Design设计规范
多形态适配：手机、平板、折叠屏完美适配
流畅动效：基于ArkUI的流畅动画体验
深色模式：完美支持系统深色模式
无障碍：全面支持无障碍功能
🛠️ 技术栈
开发环境
表格
工具	版本要求	说明
DevEco Studio	5.0+	HarmonyOS官方IDE
HarmonyOS SDK	6.0.0 (API 12)	目标SDK版本
ArkTS	1.2+	开发语言
Node.js	16.0+	构建工具依赖
核心技术
UI框架：ArkUI (声明式开发范式)
状态管理：@State/@Link/@Observed/@Provide/@Consume
数据存储：RelationalStore + Preferences
分布式能力：DistributedData + AbilityAccessCtrl
通知服务：@ohos.notificationManager
短信识别：@ohos.telephony.sms + AI文本分析
图表渲染：自定义Canvas绘制图表
生物认证：@ohos.userIAM.userAuth
权限声明
{
  "requestPermissions": [
    {
      "name": "ohos.permission.READ_SMS",
      "reason": "$string:permission_sms_reason",
      "usedScene": {
        "abilities": ["EntryAbility"],
        "when": "inuse"
      }
    },
    {
      "name": "ohos.permission.NOTIFICATION_CONTROLLER",
      "reason": "$string:permission_notification_reason"
    }
  ]
}
🚀 快速开始
环境配置
安装开发工具
# 下载 DevEco Studio
# https://developer.harmonyos.com/cn/develop/deveco-studio
配置SDK
打开 DevEco Studio → Settings → SDK Manager
安装 HarmonyOS SDK 6.0.0 (API 12)
配置 SDK 路径
获取项目代码
git clone https://github.com/your-org/rushi-subscription.git
cd rushi-subscription
编译运行
安装依赖
ohpm install
配置签名
File → Project Structure → Project → Signing Configs
勾选 "Automatically generate signature"
登录华为账号自动配置签名
连接设备
开启USB调试
连接设备并授权
确认设备已连接：
hdc list targets
运行应用
# 构建并安装Debug版本
hvigorw assembleHap --mode debug
hvigorw installHap --mode debug

# 或直接点击IDE运行按钮
发布构建
构建Release版本
# 配置Release签名后执行
hvigorw assembleHap --mode release
产物位置
entry/build/default/outputs/default/entry-default-signed.hap
上架应用市场
登录华为开发者联盟
创建应用并提交审核
发布后用户可在应用市场下载
📂 项目结构
Rushi/
├── AppScope/                    # 应用全局配置
│   ├── resources/              # 全局资源
│   └── app.json5              # 应用配置
├── entry/                      # 主模块
│   ├── src/main/
│   │   ├── ets/
│   │   │   ├── entryability/  # 应用入口
│   │   │   ├── pages/         # 页面目录
│   │   │   │   ├── Index.ets      # 首页-订阅列表
│   │   │   │   ├── AddSubscription.ets # 添加订阅
│   │   │   │   ├── Statistics.ets  # 统计分析
│   │   │   │   ├── Calendar.ets    # 日历视图
│   │   │   │   ├── Settings.ets   # 设置页面
│   │   │   │   └── Detail.ets     # 订阅详情
│   │   │   ├── components/    # 自定义组件
│   │   │   │   ├── SubscriptionCard.ets  # 订阅卡片
│   │   │   │   ├── ChartView.ets       # 图表组件
│   │   │   │   ├── WidgetProvider.ets   # 服务卡片
│   │   │   │   └── CategoryIcon.ets   # 分类图标
│   │   │   ├── model/         # 数据模型
│   │   │   │   ├── Subscription.ets   # 订阅模型
│   │   │   │   └── Category.ets       # 分类模型
│   │   │   ├── utils/         # 工具类
│   │   │   │   ├── DateUtil.ets       # 日期工具
│   │   │   │   ├── EncryptUtil.ets    # 加密工具
│   │   │   │   └── NotificationUtil.ets # 通知工具
│   │   │   ├── services/      # 服务层
│   │   │   │   ├── SubscriptionService.ets # 订阅服务
│   │   │   │   ├── ReminderService.ets     # 提醒服务
│   │   │   │   └── ImportService.ets       # 导入服务
│   │   │   └── data/          # 数据层
│   │   │       └── DatabaseHelper.ets # 数据库帮助类
│   │   ├── resources/         # 模块资源
│   │   │   ├── base/          # 基础资源
│   │   │   └── rawfile/       # 原始文件
│   │   └── module.json5       # 模块配置
│   └── build-profile.json5    # 构建配置
├── docs/                       # 文档目录
│   ├── screenshots/           # 应用截图
│   └── CHANGELOG.md         # 更新日志
├── hvigor/                     # 构建工具
├── oh_modules/                 # 依赖库
├── .gitignore
├── build-profile.json5
├── hvigorfile.ts
├── oh-package.json5
└── README.md
🤝 贡献指南
欢迎参与如时项目的贡献！无论是代码贡献、文档完善、问题反馈都非常欢迎。
如何贡献
Fork 仓库
git clone https://github.com/your-username/rushi-subscription.git
cd rushi-subscription
创建分支
# 功能开发
git checkout -b feature/new-feature

# Bug修复
git checkout -b fix/bug-description
开发与提交
# 进行代码开发

# 提交更改
git commit -m "feat: 添加邮箱账单导入功能"
提交PR
git push origin feature/new-feature
然后在GitHub上提交Pull Request
代码规范
遵循 HarmonyOS编码规范
使用 ArkTS 严格模式
保持代码简洁，注释清晰
提交前运行测试
Issue 规范
**Bug 反馈请包含：
设备型号
HarmonyOS版本
应用版本
复现步骤
预期行为
实际行为
**功能建议请说明：
功能描述
使用场景
实现思路（可选）
📄 开源协议
本项目采用 Apache License 2.0 协议开源
Apache License
Version 2.0, January 2004
http://www.apache.org/licenses/

Copyright (c) 2024 如时开发团队

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
👥 开发者
小小崔 - 主要开发
⭐ 如果这个项目对你有帮助，欢迎点个Star支持一下！
Made with ❤️ for HarmonyOS
