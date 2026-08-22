# agents-skills

## インストール
```shell
# CD
cd D:\Github\Projects
# フォルダが存在する場合は削除
if ((Test-Path -Path .\agents-skills)){rmdir .\agents-skills}
# クローン実行
git clone -b dotnet10 https://github.com/hide104y/agents-skills.git
# 配置
cd D:\Github\Projects
if (-Not (Test-Path -Path .\.agents\skills)){mkdir .\.agents\skills}
FsFileUtil.exe -a copy -m new -f agents-skills -t .agents\skills -xd "\.git$" -xf "README.md" -vv -list
FsFileUtil.exe -a copy -m new -f agents-skills -t .agents\skills -xd "\.git$" -xf "README.md" -vv
```

## ソースレビュー
- .NET 10向けモダナイズ
- xUnit による単体テスト作成
```shell
cd D:\Github\Projects
agy
/clear
「.\CmnClsLib」配下のソースに対して、スキル「source-review」を実行して
/exit
```

## ソースコードから仕様書作成
```shell
cd D:\Github\Projects
agy
/clear
「.\CmnClsLib」配下のソースに対して、スキル「spec-from-source」を実行して
/exit
```
