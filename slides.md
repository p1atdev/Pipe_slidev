---
theme: default
background: /low-poly-grid-haikei.svg
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## パイプBOT 解説スライド
  パイプ BOT のプレゼンテーション
drawings:
  persist: false
title: パイプ BOT (仮称)
---

# パイプ BOT (仮称) 

複数のメッセージアプリの会話を繋げる BOT サービス

<!-- <div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div> -->

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

<h1 class="font-bold"> <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-500 to-blue-500">パイプ BOT</span> とは？ </h1>

複数のメッセージアプリの会話を繋げる BOT サービス。

## 特長

<br />

<p class="text-2xl">
<v-clicks>

- LINE や Discord など、異なるメッセージアプリ間でメッセージを送ることができる！
- メッセージアプリの機能として提供されている、BOT 機能を利用するので、普段の使い慣れているメッセージアプリを使い続けることができる！

</v-clicks>
</p>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<!-- <style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style> -->

---

# 現状のメッセージアプリの問題点
さまざまなメッセージアプリが存在するが...

## 多人数に情報を伝える際には不便なことがある

<div class="text-2xl py-8">

<div v-click="1">

- 必ずしも、全員が同じメッセージアプリを使っている/使える訳ではない

  <div v-click="2">

    - 電話番号やスマホを持っていなければ LINE はできない 

  </div>

</div>

<!-- <div v-click="3"> -->

  <div v-click="3">

  - 全員が使っているメッセージアプリはあまりない

  </div>

  <div v-click="4" >

  - 普段使っているメッセージアプリを使いたい！

  </div>

<!-- </div> -->

</div>
 

---

# 全員が使っているツールは？

<div class="text-2xl py-6">

<div v-click="1">

- メール

  <div v-click="2">

  - 情報伝達でメールは使い慣れていない人が多そう
    - メール見ない
    - 通知に気づきにくい

  </div>

</div>

<div v-click="3">

- 電話

  <div v-click="4">

  - 多人数に連絡するには不便
    - 時間、場所が限定されてしまう

  </div>

</div>

</div>
 
<style>

</style>


---

# パイプ BOT が解決する問題

<div class="text-2xl py-6">

  <div v-click="1">

  - **普段使っているメッセージアプリ**を使って、**全員**に情報伝達ができる！

    <div v-click="2">

    - わざわざ新しいメッセージアプリに登録したり、使い方を覚える必要がない！

    </div>

  </div>

  <div v-click="3">

  - メッセージアプリの機能の差を吸収

  <div v-click="4">

   - LINE のスタンプなど

  </div>

  </div>

  <div v-click="5">

  - ひとつのメッセージアプリだけでも、さらに便利に使える

    - より高度なメッセージ管理が可能になる

  </div>

</div>

---

# LINE と Discord をつなぐ例 1

<div class="">

<img class="object-cover h-md mx-auto" src="/diagram-1.png">

</div>

---

# LINE と Discord をつなぐ例 2

<div class="">

<img class="object-cover h-md mx-auto" src="/diagram-2.png">

</div>

---

# プロトタイプの動作の様子

<img class="object-cover h-md mx-auto" src="/prototype-1.png" />

---

# 便利な使い方
ひとつのメッセージアプリのみを使う場合でもさらに便利に

<div class="flex">

<div class="flex-1">

## アナウンス専用グループ

<div class="mr-4">

現状の LINE には、グループごとにプロフィールを変更する機能や役職機能がないため、部活などのグループで、誰が部長なのかわかりにくいという問題がある。

そこで、パイプ BOT のプロフィール変換機能を利用することで、自分のアナウンス専用グループに送ったメッセージを、部活のグループにわかりやすく転送することができるようになる。

このように使うことで、わざわざプロフィールに本名や役職名を書く必要がなくなる。

</div>

</div>

<img class="object-cover h-md mx-auto" src="/diagram-3.png" />

</div>

---


# パイプ BOT の実装

<div class="flex text-2xl py-2">

<div class="flex-1">

## プロトタイプ

- Node.js (JavaScript)

- Heroku

- Firebase
  - Firestore 
  - Cloud Storage

</div>


<div class="flex-1">

## 正式実装 (予定)

- Node.js (**TypeScript**)

- Railway? Heroku? Cloud Run?

- **PlanetScale**

- **Cloudinary**

### 設定/管理アプリ

- Next.js? Blitz.js?
- Chakra UI? MUI?

</div>

</div>

---

# プロトタイプ時点でのパイプ BOT の課題

<div class="text-2xl py-4">

  <div v-click="1">

  - 特殊なイベントのハンドル

    <div v-click="2">

    - メッセージアプリごとに固有の機能やイベントがあり、それらを吸収するための工夫が必要
      - 物によっては大量にデータを保存しないといけないものもある...

    </div>

  </div>

  <div v-click="3">

  - <span class="text-4xl">**コスト**</span>

    <div class="text-3xl" v-click="4">

    - LINE Messaging API がめちゃくちゃ高い

    </div>

  </div>

</div>

---

# サービス形態の案

<div class="text-2xl py-4">

<div v-click="1">

  - OSS として公開し、各自で自分のパイプ BOT を動かすことができるようにする
    - [Strapi](https://strapi.io/) などのような形式
    - コストを抑えられる

</div>

<div v-click="2">

  - ユーザーが自分で必要な BOT の API キーを取得し、BOT の実行自体はこちら側に任せる形態
    - LINE BOT サービスの [hachidori](https://hachidori.io/) はこのような形態
    - こちらもコストを抑えられる

</div>

</div>

---


# まとめ

<div class="text-2xl">

- 多人数に情報を伝達する際、全員に伝えることが難しい場合がある

<br />

- パイプ BOT がその問題を軽減、解決できる

  - パイプ BOT は**複数のメッセージアプリ間の会話を繋げる**ことができる！

  - ひとつのメッセージアプリだけでも、**さらに便利に**使えるようになる！

<br />

- コスト的な問題から、パイプ BOT は個人で運営することは難しい

  - **OSS として公開**したり、BOT やアカウントだけはユーザーに自分で取得させる形態で公開？

</div>
