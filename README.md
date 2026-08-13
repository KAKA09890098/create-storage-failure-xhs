# 存储故障小红书图文批量创作 Skill

一个面向 ChatGPT Codex 的中文 Skill，用于批量创作原创、生活化、可执行的存储设备故障科普内容，并组织分步配图、图片卡片、独立 Word、合集 Word、检查 PDF、故事板和完整压缩包。

核心原则：**保护数据优先于修好设备。**

## 适用场景

- 机械硬盘、SSD、移动硬盘、U盘、SD卡等设备故障科普
- Windows 与 macOS 存储设备排查文章
- 小红书图文批量选题与写作
- AI 分步配图、Word/PDF 排版及完整交付包
- RAW、未初始化、未分配、0字节、掉盘、异响、误删或误格式化等故障场景

## 目录结构

```text
create-storage-failure-xhs/
├── README.md
├── LICENSE
└── skill/
    └── create-storage-failure-xhs/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── references/
            ├── content-and-delivery-spec.md
            └── safety-and-technical-rules.md
```

## 安装

下载仓库 ZIP 并解压，找到：

```text
skill/create-storage-failure-xhs
```

将整个 `create-storage-failure-xhs` 技能文件夹上传或导入 ChatGPT/Codex 的 Skills 页面。不要只上传 `README.md`，真正的技能入口是文件夹中的 `SKILL.md`。

## 使用示例

```text
@create-storage-failure-xhs

帮我制作10篇移动硬盘故障小红书文章，每篇5张图，
覆盖Windows和macOS，生成独立Word、合集Word和完整压缩包。
```

也可以直接描述任务；当请求涉及存储故障科普、小红书图文、分步排查、配图或Word/PDF交付时，Codex可以自动调用该技能。

## 主要能力

- 先判断是否需要停止通电或停止写入
- 优先使用厂商官方资料核验技术事实
- 通过选题矩阵减少批量文章重复
- 将专业术语翻译成生活化比喻，同时说明真实含义
- 同时提供 Windows 与 macOS 的小白分步排查
- 固定文章结构、图片场景和六页 Word 版式
- 导出 PDF 后逐页检查排版
- 检查文章、图片、Word、页数、总结字数和压缩包完整性

## 安全边界

该技能不会把初始化、格式化、新建卷、CHKDSK 或 macOS First Aid 描述成无风险操作。对于异响、进水、摔落、异常发热、容量错误、持续掉盘、0字节、RAW、未分配或未初始化等高风险情况，会优先要求停止通电或停止写入。

## 许可证

本项目采用 [MIT License](LICENSE)。使用、修改或分发时请保留许可证与版权声明。

## 免责声明

本项目提供的是数据安全科普与内容生产流程，不替代专业数据恢复检测。任何存储介质继续通电、写入或修复操作都可能影响数据恢复结果；重要资料应优先停止操作并评估只读镜像或专业恢复方案。

