# Office Agents

可安装、可分享的 Codex 全局办公角色包，包含协调、开发、评审、Teambition、GitLab、钉钉六个角色及三个配套技能。

**默认关闭自动更新。** 安装不会创建定时任务、后台拉取 Git 或启动项目监听。更新仅在用户手动执行时进行；定时更新须用户另行明确启用。

## 下载和安装

下载 [v1.0.0 ZIP](releases/office-agents-1.0.0.zip)，解压并进入 office-agents 目录：

```powershell
python install.py check
python install.py install
```

需要 Python 3.9+ 和支持个人自定义 Agent 的 Codex。安装后重新加载客户端验证角色可用；外部工具需自行连接、授权，项目资料按模板填写。

## 手动从 Git 更新

在保留的本地安装包目录运行：

```powershell
.\update-from-git.ps1 -RepoUrl https://github.com/whl404/office-agents.git -Ref main -CheckOnly
.\update-from-git.ps1 -RepoUrl https://github.com/whl404/office-agents.git -Ref main
```

只更新本包管理的角色和技能，保留工作区绑定、运行记录与监听开关。更新前备份；发现本地修改会停止，禁止静默覆盖。执行本地安装器，不运行下载的脚本。

详见 [安装、配置和更新说明](distribution/office-agents/README.md)。[ZIP SHA-256](releases/office-agents-1.0.0.zip.sha256)。

本包提供角色与流程指令，不包含常驻服务、业务账号、自动化授权或程序级权限隔离；部署与数据库操作仍遵守实际工具审批。
