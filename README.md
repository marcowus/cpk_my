# 竞赛刷题 Android App

内置 230 道题，完全离线：

- 大数据技术理论：50
- 深度学习理论：50
- 计算机基础理论：50
- pandas 数据处理：40
- 线性回归建模：40

## 刷题逻辑

- 单选 / 判断：点选后提交。
- 多选：勾选所有答案后提交。
- 实操题：使用“我会，下一题 / 不会，查看答案”自评。
- 答对：直接进入下一题，不弹解析。
- 答错 / 不会：立即显示内置解析，并自动加入错题本。
- 错题本复习时再次答对：自动从错题本移除。
- 错题与统计使用 Android SharedPreferences 本地保存，无需登录、无需联网。

## 构建环境

项目按 2026-08 官方 Android 文档配置：

- AGP 9.3.0
- Gradle 9.5.0
- compileSdk / targetSdk 37
- Compose BOM 2026.06.00
- Activity Compose 1.13.0
- Kotlin / Compose compiler plugin 2.3.21
- JDK 17+

直接用当前稳定版 Android Studio 打开项目即可 Sync / Run。


## 本次交付状态

- 题库 JSON：已校验 230/230。
- App 业务逻辑：已实现分类刷题、随机 20 题、五类 50 题模拟、错题本、错题解析、本地进度统计。
- 当前生成环境没有 Android SDK，因此这里没有伪造一个“已编译 APK”。
- 工程已附带 `.github/workflows/android-build.yml`：放入 GitHub 后可用 Actions 构建 debug APK。
- 也可在安装好 Android SDK 37 的 Android Studio 中打开并构建。

## APK 构建（GitHub Actions）

1. 将整个工程提交到一个 GitHub 仓库；
2. 打开仓库的 **Actions**；
3. 运行 **Build Android APK**；
4. 构建完成后下载 `BigDataQuiz-debug-apk` artifact。

> 工作流不会把题目或错题上传到服务器。App 运行时题库、错题本和进度均保存在设备本地。
