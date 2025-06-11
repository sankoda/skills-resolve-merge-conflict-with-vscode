

# Step2: マージコンフリクトを解決する

良いスタートを切っています!次に、マージ競合について詳しく見ていきましょう。🔍

これは怖いかもしれませんが、恐れることはありません、Gitはマージに関しては賢いです!Git では、競合の解決方法を決定するのに人間が必要です。場合によっては、マージの競合を解決する最善の方法は、両方のブランチからのコンテンツ、またはどちらにもないものを追加することです。これが、Git がコードを見て適切な修正を行うために人間が必要な理由です。

## ⌨️やること1: GitHub上のリポジトリをVSCodeに複製する

> 前提としてVSCodeとGitが個人端末にインストールされている必要があります。
> インストールされていない場合、GitHubのcodespaceを利用します。

1. 画面上部のタブの**Code**をクリックします。
2. 画面の中ほどにある緑色の**Code**をクリックします。
3. 表示されているURLをクリップボードにコピーします。
4. VSCodeを開きます。
5. VSCodeのターミナルを開きます。
   - 画面上部の**Terminal**をクリックします。
   - **New Terminal**をクリックします。
   - 画面下部にターミナルが表示されます。
6. ターミナルの好きなディレクトリ下で以下を実行します。
   - `git clone [コピーしたURL]`
   - リポジトリが個人端末下に複製されます。

リポジトリが複製されたことを、`ls`コマンド等で確認できます。指定がない場合リポジトリ名（URLの最後のパスの`.git`を除いた部分）がディレクトリ名となります。正常に作成されると以下のような状態になります。

```sh
[kubotako@beer-oha-kubotako011 ~]$ git clone https://github.com/kuboctopus/skills-resolve-merge-conflict-with-vscode.git
Cloning into 'skills-resolve-merge-conflict-with-vscode'...
remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (18/18), done.
remote: Compressing objects: 100% (13/13), done.
Receiving objects: 100% (18/18), 6.67 KiB | 6.67 MiB/s, done.
remote: Total 18 (delta 2), reused 13 (delta 1), pack-reused 0 (from 0)
Resolving deltas: 100% (2/2), done.
[kubotako@beer-oha-kubotako011 ~]$ 
[kubotako@beer-oha-kubotako011 ~]$ ls skills-resolve-merge-conflict-with-vscode/
LICENSE  README.md  resume.md
```

## ⌨️やること2: VSCodeで特定のディレクトリを開く

VSCodeでフォルダを開くことで、サブフォルダやエディタでのファイル表示をサポートしてくれます。

1. 画面上部タブの**File**をクリックします。
2. **Open Folder**をクリックします。
3. 複製したリポジトリ（ディレクトリ）を入力します。
4. **OK**をクリックします。

画面左側にディレクトリやファイルが表示されます。

## ⌨️やること3: VSCodeでマージコンフリクトを解決する

1. ブランチを変更します
   - VSCodeでは、リポジトリのブランチは画面下部に表示されます。（複製時はmainブランチです）
   - `git switch [ブランチ名]`でブランチを切り替えます。
   - my-resumeブランチに切り替える場合は`git switch my-resume`を実行します。
2. mainブランチの変更内容をmy-resumeブランチに取り込みます。
   - `git merge main`を実行します。
   - マージコンフリクトしたファイルは画面左側で赤く表示されるようになります。
   - コマンドの実行結果は以下のようになります。

```sh
[kubotako@beer-oha-kubotako011 skills-resolve-merge-conflict-with-vscode]$ git merge main
Auto-merging resume.md
CONFLICT (content): Merge conflict in resume.md
Automatic merge failed; fix conflicts and then commit the result.
```

1. 画面左側ファイルのresume.mdをクリックします。
2. my-resumeブランチの変更を適用するには、**Accept Current Change**をクリックします。
3. [Ctrl + S]でresume.mdを保存します。
4. 変更をステージ・コミットします。
   - 画面左タブの上から3番目の枝分かれしているアイコンをクリックします。
   ![branch icon](https://github.com/kuboctopus/resolve-merge-conflict-with-vscode/blob/main/images/branch_icon.png?raw=true)
   - 画面左側のタブのresume.mdの **+** をクリックします。
   - 青色の **Continue** ボタンをクリックします。
   - 青色の **Sync Changes 3** ボタンをクリックします。
   - ポップアップが表示されるので **OK** をクリックします。
5. 20秒ほど待ってこのページ（説明を表示しているタブ）を更新してください。GitHub Actionsが次のステップにアップデートします。


