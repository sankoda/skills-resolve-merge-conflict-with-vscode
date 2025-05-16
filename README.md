# マージコンフリクトをVSCodeで解消する

_マージコンフリクトが起きる理由と対処法を*VSCode*を用いて学びます。_

## 概要

[GitHub Skills](https://skills.github.com/) を活用することで、GitHubのGUIの利用方法を学ぶことができます。
これによりGitHubのGUIでの利用方法を理解できる一方で、実際にソースコードや文書を修正するのはVSCode等のエディタを用いること多いです。そこで重要になるのがVSCodeとGitHubの連携方法です。
このコースでは、[resolve-merge-conflict](https://github.com/skills/resolve-merge-conflicts/tree/main) と同様にマージコンフリクトを意図的に発生させ、VSCodeを用いて解決する手順を提供します。

- 学習内容：VSCodeを利用したマージコンフリクトの解決方法について。
- 作成するもの: マークダウンで書かれた要約ファイル`resume.md`を使用します。
- 前提条件：[resolve-merge-conflict](https://github.com/skills/resolve-merge-conflicts/tree/main)の内容を理解していることをお勧めします
- 所用時間: このコースの所要時間は 30 分未満です。

このコースではVSCodeを利用して以下を学びます:

1. プルリクエストを作成する
2. マージコンフリクトを解消する
3. プルリクエストをマージする

## このコースの始め方

<!-- For start course, run in JavaScript:
'https://github.com/new?' + new URLSearchParams({
  template_owner: 'kuboctopus',
  template_name: 'resolve-merge-conflict-with-vscode',
  owner: '@me',
  name: 'resolve-merge-conflict-with-vscode',
  description: 'My clone repository',
  visibility: 'public',
}).toString()
-->

[![start-course](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=kuboctopus&template_name=resolve-merge-conflict-with-vscode&owner=%40me&name=skills-resolve-merge-conflict-with-vscode&description=My+clone+repository&visibility=public)

1. **Start cource**を**右クリック**し、新しいタブでリンクを開きます。
2. 新しいタブでリポジトリを作成します。
   - 個人下にリポジトリを作成してください。（組織下に作成すると課金される可能性があるため）
   - リポジトリの公開設定はパブリックにしてください。（プライベートだとGitHub Actionsで課金されます）
3. 新しいリポジトリが作成されて20秒後にページを更新してください。ステップごとの説明がREADMEに表示されます。
