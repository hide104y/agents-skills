# agents-skills

## インストール
```shell
# CD
cd D:\Github\workspace.jre8
# フォルダが存在する場合は削除
if ((Test-Path -Path .\agents-skills)){rmdir .\agents-skills}
# クローン実行
git clone -b java08 https://github.com/hide104y/agents-skills.git
# 配置
cd D:\Github\workspace.jre8
if (-Not (Test-Path -Path .\.agents\skills)){mkdir .\.agents\skills}
FsFileUtil.exe -a copy -m new -f agents-skills -t .agents\skills -xd "\.git$" -xf "README.md" -vv -list
FsFileUtil.exe -a copy -m new -f agents-skills -t .agents\skills -xd "\.git$" -xf "README.md" -vv
```

## ソースレビュー
- 下位互換性考慮なしの修正を実施するスキル
  - メソッド名を変更した場合は、元のメソッドを非推奨メソッドとして残さないので、ソースファイル単体でこのスキルを適用しないこと。
```shell
cd D:\Github\workspace.jre8
agy
/clear
「.\chkdbconn」配下のソースに対して、スキル「source-review」を実行して
/exit
```

## ソースレビュー
- 下位互換性を考慮して修正を実施するスキル
  - メソッド名を変更した場合は、元のメソッドを非推奨メソッドとして残す。
```shell
cd D:\Github\workspace.jre8
agy
/clear
「.\chkdbconn」配下のソースに対して、スキル「source-review-libraries」を実行して
/exit
```

## 非推奨メソッドの使用排除
- 依存ライブラリーの非推奨メソッドの使用有無を確認して、非推奨メソッドの使用を発見した場合は推奨メソッドの使用へ変更するスキル
```shell
cd D:\Github\workspace.jre8
agy
/clear
「.\chkdbconn」配下のソースに対して、スキル「clean-deprecated」を実行して
/exit
```

## 依存ライブラリーの更新
- 依存ライブラリーの更新版有無を調査し、更新版があれば差し替えるスキル
- 外部ライブラリーの更新で正常機能しなくなる場合があり、エラーがでたらAIと対話が必要なので注意
```shell
cd D:\Github\workspace.jre8
agy
/clear
「.\chkdbconn」配下のソースに対して、スキル「update-dependencies」を実行して
/exit
```
