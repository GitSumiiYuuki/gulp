# Coding Template ECSS

## CSS設計
ECSS (Enduring CSS)

## 命名規則
``` namespace-Module_ChildNode-variant ```

をベースにクラス名を決める。

- namespace
  - Moduleが含まれるグループの接頭辞
- Module or Component
  - navやheaderなどの構造的機能部分
- ChildNode
  - Moduleに含まれる部品
- variant
  - バリエーション

例）```.st-Header``` , ```.sw-Tab_Item```

variantに関しては wai-aria が推奨されている。

例）```<div class="sw-Tab_Item" aria-current="true">```

## ディレクトリ構造
```
scss
├── base
│   ├── variable/
│   ├── _mixins.scss
│   └── _base.scss
├── structure
│   ├── _header.scss
│   └── _footer.scss
├── sitewide
│   ├── _btn.scss
│   └── _ttl.scss
└── namespace
    ├── layout/
    ├── _top.scss
    └── _contact.scss
```
- structure
  - サイト共通のModule ```.st-```
- sitewide
  - サイト共通のComponent ```.sw-```
- namespace
  - その他独自でつけた名前空間のスタイルディレクトリ  ```.tp-``` ,  ```.l-```
