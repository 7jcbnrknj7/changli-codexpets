# 用 GitHub 网页更新仓库

本教程假设仓库已经上传旧版，默认分支叫 `main`。如果你的默认分支叫 `master`，对应替换名称。仓库需有写入权限。

## 1. 先保存旧版分支

1. 打开仓库，进入 **Code**，确认当前分支是旧版所在的 `main`。
2. 点击文件列表上方的分支下拉菜单（通常显示 `main`）。
3. 输入 `v1-archive`，点击 **Create branch: v1-archive from main**。
4. 这个分支保存旧版；后续不要向它上传新版文件。如果旧版已经不在 main，从它对应的旧提交建立分支。

## 2. 创建新版更新分支

1. 分支菜单切回 `main`。
2. 再打开分支菜单，输入 `update/changli-v2`。
3. 点击 **Create branch: update/changli-v2 from main**。
4. 确认文件列表上方显示 `update/changli-v2`。

也可以在分支菜单选择 **View all branches → New branch**，Source 选 `main`。

## 3. 上传文件，更新同名内容

1. 解压下载的 ZIP，进入 `changli-v2-github` 文件夹。
2. 在 GitHub 的 `update/changli-v2` 分支根目录，点击 **Add file → Upload files**。
3. 把文件夹**里面的文件和 previews 子文件夹**拖进去，不要把外层 `changli-v2-github` 文件夹整体拖进去。
4. 同一路径的 `spritesheet.png`、`pet.json`、`README.md`、`.gitignore` 和已有预览会更新；`CHANGELOG.md`、`GITHUB_GUIDE.md`、新预览等会新增。
5. 如果旧版资产在子目录中，应打开那个子目录再上传，或将文件放到对应路径，避免另建重复资产。
6. 填写 Commit message：`Update Changli assets to v2.0.0`。
7. 选择提交到当前 `update/changli-v2` 分支，点击 **Commit changes** 或 **Propose changes**（按钮随页面状态变化）。

`.gitignore` 是隐藏文件，如资源管理器中看不到，启用“查看 → 显示 → 隐藏的项目”，也可单独选择上传。

ZIP 不需要上传到仓库文件区；上传解压后的内容。浏览器每个文件限制25MiB，本包全部文件均低于此限制。

## 4. 建立 Pull Request 并合并

1. 打开仓库 **Pull requests → New pull request**。
2. **base** 选择 `main`；**compare** 选择 `update/changli-v2`。
3. 查看 **Files changed**，确认精灵图、元数据和 README 更新到了正确路径。
4. 点击 **Create pull request**，标题填写 `长离 v2：知性温柔版`。
5. 描述可写：`保留v1，更新写信与信鸽、撑伞回眸、伸手互动；移除眨眼大笑和跳跃。显示名称为长离。`
6. 检查完成后点击 **Merge pull request → Confirm merge**。如果仓库要求审核或检查，先满足这些条件。
7. 回到 Code 切回 `main`，查看 README 图片和最新精灵图。
8. 合并后可删除临时 `update/changli-v2` 分支；保留 `v1-archive`。

## 5. 可选：发布 v2.0.0 Release

进入仓库 **Releases → Draft a new release**，新建标签 `v2.0.0`，目标选择已经合并新版的 `main`，标题填 `长离 v2.0.0`，说明复制 CHANGELOG 的2.0.0段落，可把ZIP作为下载附件，再发布。

版本号和分支不是一回事：`v2.0.0` 是发布标签，`update/changli-v2` 是此次修改的工作分支，`main` 是合并后的当前版本。

## 后续更新

以后每次从最新 `main` 建立新分支，例如 `update/changli-v2-1`；上传修改的同名文件，更新版本号与 CHANGELOG，提交、建立PR、合并即可。新分支会从选定的来源复制当前提交，不是空文件夹。

## GitHub 官方参考

- [建立分支](https://docs.github.com/en/pull-requests/how-tos/commit-changes/managing-branches-within-your-repository)
- [上传文件](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
- [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow)
