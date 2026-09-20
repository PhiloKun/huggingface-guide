# Hugging Face 操作指南

一份面向中文网络环境的 Hugging Face 实操手册，单文件 HTML，图文并茂，可直接离线打开或打印。

| 位置 | 地址 |
| --- | --- |
| 在线访问（GitHub Pages） | https://philokun.github.io/huggingface-guide/ |
| GitHub 仓库 | https://github.com/PhiloKun/huggingface-guide |
| Gitee 镜像 | https://gitee.com/PhiloKun/huggingface-guide |

> Gitee 侧仅作代码镜像。Gitee Pages 已被官方标记为功能下线，站点只在 GitHub Pages 发布。

## 这份指南解决什么问题

网上的 Hugging Face 教程大多停留在 2025 年年中之前，里面的 `huggingface-cli` 命令**现在已经跑不通了**。本指南基于当前版本重写，重点标注了容易踩坑的版本变更与国内网络环境下的实操细节。

覆盖内容：

- 生态三层结构（本地工具 / 云端 Hub / 上层生态）
- 安装与登录（`hf` CLI 与 `hf auth` 子命令）
- 模型与数据集下载：完整命令、参数表、7 个常见场景示例
- 本地缓存机制：`blobs` 真实文件与 `snapshots` 软链接视图的关系，以及缓存清理
- 国内网络加速：`HF_ENDPOINT` 镜像方案与验证方法
- 上传与仓库管理：`hf upload`、大目录续传、git + LFS 路线、buckets
- Python 调用：`transformers` 与 `huggingface_hub` 代码示例
- Spaces 应用部署：目录结构、front matter 配置、更新流程
- 排障速查表（13 条常见故障）与一页速查卡

## 内容特色

| 特点 | 说明 |
| --- | --- |
| 图 | 3 张内联 SVG 图示：生态分层、缓存目录结构、镜像加速链路对比 |
| 结构 | 全文按「命令 → 参数 → 示例」组织，参数单独成表 |
| 版本 | 明确标注 `huggingface-cli` 移除、transformers v5 只支持 PyTorch、TGI 归档等变更 |
| 适配 | 表格与图均内联，支持深色模式自动适配与打印分页 |

## 版本适用范围

核对时间：2026-09。适用于 `huggingface_hub >= 1.0`、`transformers >= 5.0`。

CLI 迭代很快（官方已是每周发布节奏），遇到参数对不上时以本地 `hf <命令> --help` 的实际输出为准。

## 本地查看

```bash
# 直接用浏览器打开即可，无任何依赖
open index.html

# 或起一个本地服务
python3 -m http.server 8000
# 然后访问 http://localhost:8000
```

## 目录结构

```
.
├── index.html    # 完整指南（单文件，含内联 CSS / SVG）
├── .nojekyll     # 阻止 GitHub Pages 用 Jekyll 处理，确保文件原样发布
└── README.md
```

## 部署

站点通过 GitHub Pages 发布，源为 `main` 分支根目录。

## 参考

- 官方文档：https://huggingface.co/docs/huggingface_hub
- 国内镜像：https://hf-mirror.com
- Token 管理：https://huggingface.co/settings/tokens

## License

MIT
