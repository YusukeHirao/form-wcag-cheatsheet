# フォーム アクセシビリティガイドライン チートシート

このチートシートは、WCAG2.0 および 2.1 の「[ガイドライン 3.3 入力支援: 利用者の間違いを防ぎ、修正を支援すること。](https://waic.jp/docs/WCAG20/Overview.html#minimize-error)」を基準にウェブサイト・ウェブアプリにおける **フォーム要素の要件定義・デザイン・実装の参考になるようにまとめたもの** です。（3.3 に関しては 2.0 版 と 2.1 版 に差はありません）

## エラーの場合、テキストで説明される (3.3.1) [A] &amp; 修正の提案ができる (3.3.3) [AA]

> [3.3.1](http://waic.jp/docs/UNDERSTANDING-WCAG20/minimize-error-identified.html) **エラーの特定**: 入力エラーが自動的に検出された場合は、エラーとなっている箇所が特定され、そのエラーが利用者にテキストで説明される。 (レベル A)

> [3.3.3](http://waic.jp/docs/UNDERSTANDING-WCAG20/minimize-error-suggestions.html) **エラー修正の提案**: 入力エラーが自動的に検出され、修正方法を提案できる場合、その提案が利用者に提示される。ただし、セキュリティ又はコンテンツの目的を損なう場合は除く。 (レベル AA)

**テキストであること**: 全盲・色覚障害への知覚のため、認知・言語・学習障害のために **アイコンや画像のみは避ける** 。

### 参考:

- エラーの通知: `aria-invalid` [[ARIA21](https://waic.jp/docs/WCAG-TECHS/ARIA21.html)]
- 支援技術に通知: `role="alert`, `aria-live`, `aria-atomic` [[ARIA19](https://waic.jp/docs/WCAG-TECHS/ARIA19.html)]
- エラー箇所に移動 [[G139](https://waic.jp/docs/WCAG-TECHS/G139.html)]
- ダイアログを使う場合: `aria-alertdialog` [[ARIA18](https://waic.jp/docs/WCAG-TECHS/ARIA18.html)]
- 修正候補 [[G177](https://waic.jp/docs/WCAG-TECHS/G177.html)]

## ラベルまたは説明 (3.3.2) [A]

> [3.3.2](http://waic.jp/docs/UNDERSTANDING-WCAG20/minimize-error-cues.html) ラベル又は説明: コンテンツが利用者の入力を要求する場合は、ラベル又は説明文が提供されている。 (レベル A)

### 参考:

- `label`要素と関連付ける [[H44](https://waic.jp/docs/WCAG-TECHS/H44.html)]
- 視覚的にも近くに置く [[G162](https://waic.jp/docs/WCAG-TECHS/G162.html)]
- 認知・言語・学習障害のために **例** があるとよい [[G89](https://waic.jp/docs/WCAG-TECHS/G89.html)]
- フォーマット（書式・形式）に頼らない [[F82](https://waic.jp/docs/WCAG-TECHS/F82.html)]
- 説明: `aria-describedby` [[ARIA1](https://waic.jp/docs/WCAG-TECHS/ARIA1.html), [ARIA9](https://waic.jp/docs/WCAG-TECHS/ARIA9.html)]
- グルーピング: `fieldset`, `legend`, `aria-describedby`, `role="radiogroup"` [[ARIA17](https://waic.jp/docs/WCAG-TECHS/ARIA17.html)]
- 必須項目: `aria-required` [[ARIA2](https://waic.jp/docs/WCAG-TECHS/ARIA2.html)]
- `label`要素の代替（最終手段）: `title`属性 [[H65](https://waic.jp/docs/WCAG-TECHS/H65.html)]

## ヘルプ (3.3.5) [AAA]

> [3.3.5](http://waic.jp/docs/UNDERSTANDING-WCAG20/minimize-error-context-help.html) **ヘルプ**: コンテキストに応じたヘルプが利用できる。 (レベル AAA)

### 参考:

- ヘルプページの用意 [[G71](https://waic.jp/docs/WCAG-TECHS/G71.html)]
- アシスタントロボット（アバター） [[G193](https://waic.jp/docs/WCAG-TECHS/G193.html)]
- スペルチェック [[G194](https://waic.jp/docs/WCAG-TECHS/G194.html)]
- 説明をきちんとする → [[達成基準 3.3.2](http://waic.jp/docs/UNDERSTANDING-WCAG20/minimize-error-cues.html)]

## エラー回避（取り消しできる or 修正する機会がある or 見直しができる） (3.3.4) [AA] &amp; (3.3.6) [AAA]

> [3.3.4](http://waic.jp/docs/UNDERSTANDING-WCAG20/minimize-error-reversible.html) **エラー回避 (法的、金融、データ)** : 利用者にとって法律行為もしくは金融取引が生じる、利用者が制御可能なデータストレージシステム上のデータを変更もしくは削除する、又は利用者が試験の解答を送信するウェブページでは、次に挙げる事項のうち、少なくとも一つを満たしている: (レベル AA)
>
> 1. **取消**: 送信を取り消すことができる。
> 2. **チェック**: 利用者が入力したデータの入力エラーがチェックされ、利用者には修正する機会が提供される。
> 3. **確認**: 送信を完了する前に、利用者が情報の見直し、確認及び修正をするメカニズムが利用できる。

> [3.3.6](http://waic.jp/docs/UNDERSTANDING-WCAG20/minimize-error-reversible-all.html) **エラー回避 (すべて)** : 利用者に情報の送信を要求するウェブページでは、次に挙げる事項のうち、少なくとも一つを満たしている: (レベル AAA)
>
> 1. **取消**: 送信を取り消すことができる。
> 2. **チェック**: 利用者が入力したデータの入力エラーがチェックされ、利用者には修正する機会が提供される。
> 3. **確認**: 送信を完了する前に、利用者が情報の見直し、確認及び修正をするメカニズムが利用できる。

### 参考:

- 送信後にキャンセル（一定期間） [[G164](https://waic.jp/docs/WCAG-TECHS/G164.html)]
- 正常なときもフィードバック [[G199](https://waic.jp/docs/WCAG-TECHS/G199.html)]
