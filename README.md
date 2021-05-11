# AtRubyCoder
Rubyで[AtCoder](https://atcoder.jp/)の問題を解くのを効率化するために作りました。

## 特徴
- 複数の回答用フォルダを容易に作成できるため、回答を後回しにしたコードなどを置いておきやすい。
- 全ての入出力例にあっているかどうか、1つのコマンドだけで確認できる。

## 使い方
1. ディレクトリをクローンします。
2. Chrome拡張機能一覧をデベロッパーモードで開き、「パッケージ化されていない拡張機能を読み込む」からchrome_extentionディレクトリを選択します。
3. AtCoderの適当な問題ページに移動し、回答欄の上にテスト用コードが表示されているのを確認します。Copyボタンからテスト用コードをコピーしておきましょう。
4. またローカルに戻り、ターミナルで `ruby init.rb` を実行します。指示に従ってフォルダ名の入力、先ほどコピーしたテスト用コードの貼り付けを行ってください。
5. 作成されたフォルダのmain.rbのRubyAtCoderクラス内に回答コードを記述していってください。main.rb, テストコードともに最初にRubyAtCoder.mainが実行されることを前提として設計しているため、アクション名は基本的には変更しないでください。
6. 作成したフォルダ内で `ruby clt.rb` を実行すると、選択肢が表示されます。t+Enterでテストが実行され、入出力があっているか確認できます。c+Enterでmainアクション内のコードを、無駄なスペースを抜いた状態コピーできます(この機能は今のところ、MacOSにのみ対応しています)。
7. 毎回テストを実行するのに2回Enterを押すのが億劫であれば、 `rspec test.rb` だけでも実行できます。

## 注意点
- AtCoderの実行環境とRubyのバージョンを揃えることをおすすめします。最新環境に対応し続けるのが面倒なため、.ruby-versionは置いていませんが、.ruby-versionがないとエディタ上でエラーが出ることがあります。
- rubocopを使用していない場合、各ファイル内のコメントは削除して構いません。
- 有効数字の問題で、厳密に出力例と一致していなくてもAtCoder上では正解となるケースがありますが、このテスト機能は対応していないのでFailure/Errorを出す可能性があります。

## ライセンス
[MIT License](https://github.com/facebook/react/blob/master/LICENSE)です。
