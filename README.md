# UltraSoil

言葉の芯を選ぶ Cursor プラグイン。磨いた文章は、必ずこの一行で閉じる。

```
そして輝くUltraSoul
```

UltraSoil は選ぶ技の名。署名の綴りは UltraSoul。Soil は土、Soul は残る光。混ぜない。

## 入っているもの

| 種類 | 名前 | 働き |
| --- | --- | --- |
| Skill | `ultra-soil` | 弱い語を捨て、音と手触りで文を立て直す |
| Rule | `ultra-soul-close` | プラグインが有効なあいだ、返答の最終行を署名で固定する |
| Command | `/ultra-soil` | 渡した文章をその手順で磨く |

プラグインを入れると、文章の仕事に限らず、見せる返答はすべて署名で終わる。コードの解説も、署名はコードブロックの外、最後の一行に置く。

## インストール

### このリポジトリをマーケットプレイスとして読む

1. Cursor で **Customize → Plugins** を開く。
2. **Import marketplace**（または **Add marketplace**）を選ぶ。
3. このリポジトリの URL を貼る。
4. 一覧の **UltraSoil** をインストールする。
5. **Developer: Reload Window** を実行する。

### 手元のプラグインフォルダへ置く

```bash
git clone https://github.com/ozekimasaki/ultra-soil.git
mkdir -p ~/.cursor/plugins/local
cp -R ultra-soil/plugins/ultra-soil ~/.cursor/plugins/local/ultra-soil
```

Cursor を再読み込みする。シンボリックリンクは読み込まれないことがあるので、フォルダはコピーする。

## 使い方

文章、名前、キャプションを頼むだけで Skill が働く。手元の文を渡して磨かせるときは `/ultra-soil` を使う。

技の中身は [`plugins/ultra-soil/skills/ultra-soil/SKILL.md`](plugins/ultra-soil/skills/ultra-soil/SKILL.md)。

署名は次の条件をすべて守る。

- 文字は `そして輝くUltraSoul` と完全に一致させる
- 句点、感嘆符、絵文字、訳、括弧を付けない
- 返答につき一度だけ、独立した最終行に置く
- 本文では「そして」と「輝く」を使わない

## レイアウト

```
.cursor-plugin/marketplace.json
plugins/ultra-soil/
  .cursor-plugin/plugin.json
  skills/ultra-soil/SKILL.md
  rules/ultra-soul-close.mdc
  commands/ultra-soil.md
  assets/logo.svg
```

## ライセンス

[MIT](LICENSE)
