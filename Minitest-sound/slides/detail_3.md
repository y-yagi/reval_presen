### MinitestのExtensionの作り方

* ファイル名
  * `minitest/XXX_plugin.rb`という名前にする。
  * minitest本体で`Gem.find_files("minitest/*_plugin.rb")`を行っており、上記命名規則に則ると自動でrequireしてくれる
* 初期化処理
  * `plugin_XXX_init`という名前のメソッドを定義すると、テスト起動時に自動で呼び出される。`XXX`の部分は、ファイル名と一緒である必要がある。違うと呼ばれないので注意が必要。
* オプションの設定
  * `plugin_XXX_options`という名前のメソッドを定義すると、こちらもテスト起動時に自動で呼び出される。`XXX`については、初期化処理同様ファイル名と合わせる必要あり。
