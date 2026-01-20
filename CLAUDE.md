# Shoplazza Landing Pages - AI 编辑指南

这是一个存放 AI 生成的 Shoplazza Landing Page 主题的 monorepo。

## 目录结构

```
workshops/
└── {workshop-id}/           # 营销活动 (如 spring-festival)
    └── {project-id}/        # 项目 (如 landing)
        └── {version-id}/    # 版本 (如 v1, v2, ...)
            ├── metadata.json
            └── theme/       # Shoplazza 主题
                ├── sections/
                │   └── page_detail.liquid  ← 主要编辑目标
                ├── templates/
                ├── assets/
                ├── config/
                └── snippets/
```

## 编辑规则

1. **只编辑 theme/ 目录下的文件**
2. **主要编辑 `sections/page_detail.liquid`**
3. **保持 `{% schema %}` 部分完整**
4. **CSS 使用内联 `<style>` 标签**

## Git 工作流

1. 从 main 分支创建 feature 分支
2. 编辑文件后提交
3. 推送并创建 PR
4. 人工审核后合并
5. 合并后自动部署到 Shoplazza

## 提交信息格式

```
feat({project}): {简短描述}
```

示例:
- `feat(landing): 把标题改成红色`
- `feat(landing): 添加倒计时组件`
