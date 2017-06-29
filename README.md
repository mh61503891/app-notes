# Rails Notes



## i18n-js

* GitHub: https://github.com/fnando/i18n-js
* Railsのi18nの訳文ファイルをJavaScriptで使用する場合に便利なgemです。
* Railsの `locales/*.yml` から `translations.js` 書き出すrakeタスクが追加される。
* `translations.js` をJavaScriptから `I18n.t('js.hello');` とかで使用する。
* Rails 5.1でWebpackerが導入されたが訳文ファイルをRailsファーストにするかJavaScriptファーストにするか悩む。
    * ポイント: JavaScriptファーストにする場合はRailsをAPIモードにしてユーザ向けのメッセージを排除できるか？
* Link: http://d.hatena.ne.jp/a_kimura/20120221/1329825267

commands:

```bash
$ rails i18n:js:setup
$ rails i18n:js:export
```

config/i18n-js.yml:

```yml
translations:
  - file: 'app/assets/javascripts/i18n/translations.js'
    only: '*'
```
