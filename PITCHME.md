---

## フロントエンド出身の
## データ分析者が始めた
## ポートフォリオ

---

## はじめに

---

### 自身のポートフォリオ持っていますか？
持ってたらmiroに貼ってください！見たいです！

---

### お前、誰よ

- 株式会社メンバーズ
    メンバーズデータアドベンチャーカンパニー
- データエンジニア、アナリスト
- 大学時代にWebエンジニア

<hr>
[Portfolio](https://yasshi-lab.tech/)<br>
![Portfolio](qr20200630152708240.png)

---

### どんな人間？
- 自分が一番格下な環境を好む
    - 勉強会
    - Atcoder(5)
- 多趣味(ゲーム、ギター、バイク、PC)
- Twitter大好き

@yasshi_dayooon

---

### よくあるポートフォリオの用途

@ul
- スキルの誇示(ノーマル)
    - エンジニアリング力
    - 言語ごとの経歴
    - ...などなど
- 技術ブログ(レア)
- 発表スライドのまとめ(レア)
- 自分で作った便利ツール(激レア)
@endul

---

### 駆け出しエンジニア == ポートフォリオ?

@ul
- 駆け出しエンジニアはポートフォリオを作っているらしい
- 作って終わり　の人も多い
@endul

---

### データ分析者、マーケターにオススメのポートフォリオ
#### Google Analyticsでトラッキングする
@ul
- 1アクションに対する反応、継続している反応が可視化
- 生データで分析、ディレクション
- 実務してなくてもそこそこ学べる
@endul

---

### ポートフォリオ作る上のインプット
@ul
- Google Analytics
- クロスドメイントラッキング
    - Vue CLIでの設定、Wordpressでの設定
- Twitterカード
- SEO対策
@endul

---

### クロスドメイントラッキング

+++

#### 目的
ポートフォリオサイトとブログサイトのトラッキングを統一する
- https://yasshi-lab.tech/
- https://blog.yasshi-lab.tech/

+++

#### 現状整理
https://yasshi-lab.tech/
- Vue CLI
- firebase hosting

https://blog.yasshi-lab.tech/
- なんかよくあるWordpressホスティングサイト

+++
#### 問題と解決法
Vue CLI
- yarn build後のdist/下にできるindex.htmlのhead終了直前にトラッキングコード
    - vue-analyticsを使用することで解決

Wordpress
[ググったら出てくる方法](https://wacul-ai.com/blog/access-analysis/google-analytics-setting/wp-ga/)　でOK

+++
#### vue-analytics

```js
import VueAnalytics from "vue-analytics";

Vue.use(VueAnalytics, {
  id: process.env.VUE_APP_GA_MEASUREMENT_ID,
  router,
  linkers: ["https://yasshi-lab.tech/", "https://blog.yasshi-lab.tech/"]
});
```

+++
