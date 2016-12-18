# Jekyll test
## permalinkの問題点
**問題: トレイリングスラッシュ以降に任意の文字列を含めてもファイルが閲覧できてしまう**

`permalink: :title` としたとき、ホームからの記事へのリンクは `http://localhost:4000/welcome-to-jekyll` となっているが、`http://localhost:4000/welcome-to-jekyll/hoge` でアクセスしても同じファイルが見れてしまう。

極端な例をあげれば、`http://localhost:4000/welcome-to-jekyll/hoge/huga/piyo/aaa/bbb/ccc` などの適当なURLでも、`welcome-to-jekyll/` までが合っていればなんでもいいことになってしまう → **とてもださい**

**結論: GitHub Pages なら問題なく動作する**

ローカル開発環境ではなんとなく気持ち悪いルーティングになってしまうが、GitHub Pages にデプロイすればこの問題は解消できるのでとりあえずOKとする。
