# twitter_timeline.inc.php

WIKIWIKI.jpさんの [TwitterTimeline](https://wikiwiki.jp/sample/?TwitterTimeline) プラグインと同等の機能を PukiWiki プラグインで実装してみたモノです。
[publish.twitter.com](https://publish.twitter.com/) で生成できる埋め込みタイムラインを wiki 内に導入します。

古くからあるPukiWiki用Twitterプラグインとして佐藤 潔さんの twitter.inc.php が有名ですが、Twitter API 1.1への移行により使用できなくなったので代用として作りました。

動作確認: PukiWiki 1.4.7

## 設置方法

twitter_timeline.inc.php を plugin ディレクトリに置いてください。

## つかいかた

WIKIWIKI.jp さんのとほぼ同じですが、`link_color` の指定はできません。

## 書式

```pukiwiki
// ブロック要素
#twitter_timeline(各種パラメータ)

// インライン要素
&twitter_timeline(各種パラメータ);
```

## 引数

| パラメータ | 説明 | 省略時 | 例 |
| --------- | ---- | ----- | -- |
| @ | 表示したい Twitter アカウントのIDを@抜きで指定してください。 | (省略不可) | `@=kaz_ic` |
| width | 横幅 [px]。最大は1200です。 | 1200 | `width=100` |
| height | 高さ [px]。 | 600 | `height=300` |
| theme | テーマ色。lightとdarkの2種。 | light | `theme=dark` |
| lang | ウィジェットの表示言語を指定します。 | ja | `lang=en` |

### 指定可能な表示言語

en, ar, bn, zh-cn, zh-tw, cs, da, nl, fil, fi, fr, de, el, he, hi, hu, id, it, ja, ko, msa, no, fa, pl, pt, ro, ru, es, sv, th, tr, uk, ur, vi

## 使用例

```pukiwiki
**Twitter
CENTER:&twitter_timeline(@=kaz_ic,theme=dark);
```
