# 📚 考研单词学习应用

一个基于 Android 的考研高频词汇学习应用，采用科学记忆算法帮助用户高效记忆单词。

## ✨ 核心功能

### 🎯 科学记忆算法
- **1-2-4-7天间隔重复**：基于艾宾浩斯遗忘曲线
- **4次复习完成**：完成4次复习后标记为"认识"
- **失败重来机制**：复习失败的单词重新从第1阶段开始

### 📊 三大学习界面
1. **学习界面** - 新单词学习
2. **复习界面** - 按计划复习到期单词
3. **概览界面** - 单词状态管理和分组查看

### 🗄️ 数据管理
- **Room数据库**：本地持久化存储
- **初始词库**：20个考研高频词汇
- **单词状态**：认识/不认识/复习中/隐藏
- **自定义词库**：支持导入自定义CSV词书

## 🚀 快速开始

### 环境要求
- Android Studio
- Java 11+
- Android SDK

### 构建步骤
```bash
# 克隆项目
git clone https://github.com/Daxxsc/wordsapp.git

# 打开Android Studio导入项目
# 点击 Build → Make Project
```

### 运行应用
```bash
# 构建调试APK
./gradlew assembleDebug

# APK位置
app/build/outputs/apk/debug/app-debug.apk
```

## 📁 项目结构

```
app/src/main/
├── java/com/example/words/
│   ├── data/           # 数据层（Room数据库、Repository）
│   ├── viewmodel/      # ViewModel
│   ├── ui/            # UI界面（三个Fragment）
│   └── MainActivity.kt # 主Activity
├── res/               # 资源文件
└── assets/           # 词库CSV文件
```

## 🔧 技术栈

- **语言**: Kotlin + Java
- **架构**: MVVM + Repository
- **数据库**: Room
- **构建**: Gradle + Android Gradle Plugin
- **UI**: Navigation Component, ViewBinding

## 📖 使用指南

### 1. 学习新单词
- 进入"学习"界面
- 点击显示/隐藏翻译
- 选择"认识"或"不认识"
- 认识的单词进入复习流程

### 2. 复习单词
- 进入"复习"界面
- 系统自动显示到期单词
- 完成1-2-4-7天四次复习
- 失败则重新从第1天开始

### 3. 管理词库
- 进入"概览"界面
- 查看所有单词状态
- 分组管理（认识/不认识/复习中/隐藏）
- 支持展开/收起分组

### 4. 自定义词库
1. 创建 `my_words.csv` 文件
2. 格式：`英文单词,中文释义`
3. 放置到 `app/src/main/assets/` 目录
4. 应用会自动加载自定义词库

## 🔧 开发指南

### 项目配置
- **编译SDK**: 34 (Android 14)
- **最低SDK**: 24 (Android 7.0)
- **目标SDK**: 34
- **Java版本**: 11

### 依赖库
```gradle
// Room数据库
implementation 'androidx.room:room-runtime:2.6.1'
kapt 'androidx.room:room-compiler:2.6.1'

// ViewModel和LiveData
implementation 'androidx.lifecycle:lifecycle-viewmodel-ktx:2.7.0'
implementation 'androidx.lifecycle:lifecycle-livedata-ktx:2.7.0'

// Navigation组件
implementation 'androidx.navigation:navigation-fragment-ktx:2.6.0'
implementation 'androidx.navigation:navigation-ui-ktx:2.6.0'

// Coroutines
implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-android:1.7.3'
```

### 图标生成
如需替换应用图标，请参考 [ICON_GENERATION.md](ICON_GENERATION.md)

## 📄 文档

- [AGENTS.md](AGENTS.md) - OpenCode代理指令文档
- [ICON_GENERATION.md](ICON_GENERATION.md) - 应用图标生成指南
- [PROJECT_DOCS.md](../PROJECT_DOCS.md) - 详细项目文档（原仓库）

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📞 联系

如有问题或建议，请提交 Issue 或联系项目维护者。

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

---

**让记忆更科学，让学习更高效！** 🚀