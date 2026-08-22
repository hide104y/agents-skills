# agents-skills

## インストール
```shell
# CD
cd D:\Github\workspace.jre7
# フォルダが存在する場合は削除
if ((Test-Path -Path .\agents-skills)){rmdir .\agents-skills}
# クローン実行
git clone -b java07 https://github.com/hide104y/agents-skills.git
# 配置
cd D:\Github\workspace.jre7
if (-Not (Test-Path -Path .\.agents\skills)){mkdir .\.agents\skills}
FsFileUtil.exe -a copy -m new -f agents-skills -t .agents\skills -xd "\.git$" -xf "README.md" -vv -list
FsFileUtil.exe -a copy -m new -f agents-skills -t .agents\skills -xd "\.git$" -xf "README.md" -vv
```

## ソースレビュー
- antを用いたビルドを対象
- ソースコードをJava7に最適化
```shell
cd D:\Github\workspace.jre7
agy
/clear
「.\NwConnHostInfo」配下のソースに対して、スキル「source-review」を実行して
/exit
```
