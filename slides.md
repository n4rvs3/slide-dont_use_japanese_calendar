---
theme: purplin
highlighter: shiki
lineNumbers: false
transition: slide-left
title: 和暦をやめませんか？(切実)
mdc: true
layout: intro
position: left
---

# 和暦をやめませんか？(切実)

2024/02/09 n4rvs3

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    次へ進む <carbon:arrow-right class="inline"/>
  </span>
</div>

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: quote
position: center
---

## Attention

本スライドは一個人の所感を元に作成されています。

特定の個人・団体に向けた内容ではないことを予めご了承ください。

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: quote
position: center
---

## こんなこと思ったことありませんか？

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: image-x
image: 'https://2.bp.blogspot.com/-5iAeI3keuUc/WQA-LdnYJnI/AAAAAAABD5s/N7JKSqu2EMA52fN1wNgP8GmxGKJ2wkHhwCLcB/s800/pose_atama_kakaeru_man.png'
imageOrder: 2
---

### 和暦を扱う際の苦悩

<br />

- **逆算** - 昭和⚪︎年って西暦何年だっけ？
  - 逆も然り
- **実装** - 実装が手間だ・・・
- **メンテナンス** - 元号が変わった際のメンテナンスが・・・

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: quote
position: center
---

# 現実は甘くない

多くの公共機関では和暦が利用されています。

上記に伴いアプリケーション側でも和暦対応を求められるシーンは多いのです・・・。

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: quote
position: center
---

## なのでこんなものを作りました　:waiwai:

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: image-x
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjUF9l4BpMLj67ZckTKiASOPxsVpADYGZvV7wrNxUmE9nbgKOSieF9Kzzxqjm27IffqG0Te87P2Zdp7xo-0neAinwfG30KYS8W9-MtH2RjbcRwHlM_nKeTJNM7IY5J2WAEyvTlRS-nfXXLVrFrYrpvb7JrCp1BuRYvQyg8mvdfZNju-0A0QdS8jpAK2tw/s832/ai_dance_character.png
imageOrder: 1
---

## Japanese_Calendar_Converter

和暦と西暦をよしなに変換してくれるライブラリ

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: quote
position: center
---

## さっそく使ってみましょう

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---

<div class="flex items-center justify-around h-100">

## インストール方法(2024/02/13公開予定)

```zsh
yarn add japanese_calendar_converter
```

</div>

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---

<div class="flex flex-col justify-center items-center h-100">

## 和暦を西暦に変換

<br />

```ts
const sample = toGregorioEra({
  data: {
    era: '昭和',
    year: 64,
    month: 1,
    date: 7,
  }
})

console.log(sample)

// sample = {
// error: null;
// data: { 
//  year: "1989-01-07",
// }
```

</div>

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---

<div class="flex flex-col justify-center items-center h-100">

## 西暦を和暦に変換

(2024/02/09現在、BugFix中なので動作しません)

<br />

```ts
const sample = toJapaneseEra(19890107);

console.log(sample)

// sample = {
//  error: null;
//  data: {
//   era: '昭和',
//   year: 64,
//   month: 1
//   date: 8
//  }
// }
```

</div>

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: image-x
image: https://blogger.googleusercontent.com/img/a/AVvXsEgi8IFwR7VoUtQIBHY5U5UueeRusSawWoAD3njzwc7gR-gFyFlzPafCOHmZ7jrBxAVn2AVHWmPL8sxlm0cnxeVZbtr6zJzrEZPGLSbY4ceSaPw15CalNXNx9tk3hBtV3KFGe8CNloo0Kd-M-WI1KjJjfVGDvo3nPH-UJj6n3_9g7OhJZha8uKL6H2kpPg=s911
imageOrder: 2
---
## 利用シーン

<br />

1. 1 - フォームは和暦で入力したい
2. 2 - DBにはDate型で保存したい
   1. - toGregorioEra関数で西暦に変換できます
3. 3 - 呼び出して表示するときはx和暦で表示したい
   1. - toJapaneseEra関数で和暦に変換できます
4. 4 - バリデーションの実装がつらい
   1. - 各関数毎にてバリデーションを行い、適切なエラーを返します


<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---

## 各関数毎にてバリデーションを行い、適切なエラーを返します

例えば、存在しない日付を渡してみましょう

```ts
const sample = toGregorioEra({
  data: {
    era: '昭和',
    year: 64,
    month: 1,
    date: 8,
  }
})
```

昭和は64年1月7日まで、1月8日は平成ですので下記値がreturnされます

```ts
console.log(sample)

// sample = {
// error: "昭和64年は1月7日までです。"
// data: { 
//  year: null,
// }
```

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---

## その他エラー(toGregorio関数の例)

<br />

- 存在しない元号を渡した場合

```ts
throw new Error('元号 ' + era + ' は存在しません。');
```

- 入力された日付が存在しない場合(例: 2/31)

```ts
throw new Error(yyyymmdd + ' は存在しない日付です。');
```

- 入力された年に入力された日付が存在しない場合(例: 2024/02/31)

```ts
throw new Error(era + ' ' + year + '年' + month + '月' + date + '日は存在しません。');
```

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>

---
layout: quote
position: center
---

# 和暦と仲良くなる日をめざして

本パッケージを用いて快適な和暦ライフをお送りください😇

また、本パッケージはOSSとして公開していますので、

右下のリポジトリまでお気軽にissueやPR等お待ちしております。

<span class="text-xs">

~~そもそも和暦を採用する現場が減って欲しい所存ではありますが...~~

</span>

<BarBottom  title="和暦を辞めませんか？(切実)">
  <Item text="n4rvs3/japanese_calender_converter">
    <carbon:logo-github />
  </Item>
  <Item text="Squl_d">
    <carbon:logo-twitter />
  </Item>
</BarBottom>