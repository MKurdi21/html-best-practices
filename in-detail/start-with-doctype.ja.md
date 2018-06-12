# DOCTYPEを書く

DOCTYPEは標準モードを有効にするために必要です。

悪い例:

    <html>
      ...
    </html>

良い例:

    <!DOCTYPE html>
    <html>
      ...
    </html>


## 解説

仕様においてDOCTYPEそのものにはもはや意味はほとんどありません。これは過去、現在、そして残念ながら未来のブラウザーとの互換性のためだけに存在します。しかしながらDOCTYPEを書くことにより、仕様に基いた形でHTML文書がレンダリングされるようになることを保証されるはずなので、必ず書くようにするべきです。

ではこのDOCYPEを書かないとどうなるのでしょうか？

ブラウザーには[*モード*というとても残念な仕組み][1]があり、そしてこれからもあり続けることでしょう。このモードとは標準仕様に基いてレンダリングすると表示が崩れてしまうウェブページを、HTMLを修正することなくどうにかうまく表示してやろうという対策の結果の産物です。モードそのものはどうしようもない過去のしがらみとも言えますが、問題はこのモードの切り替えにDOCTYPEのあるなしが流用されているということです。その流用の結果、HTML文書へDOCTYPEを書かない場合に仕様とは互換性のない形でレンダリングされてしまうという不幸な仕組みになってしまいました。

この仕様と互換性のないレンダリングについて正確に知ることは困難を極めます。単に昔の仕様に基づいたものであるだけでなく、過去のブラウザーにおけるバグをも内包するものだからです。つまりこのモードでレンダリングされてしまうと（DOCTYPEを書かないと）、どのようにレンダリングされるかは経験と勘というとても曖昧なものでしか判断できないことになります。チームが関わるようなケースでは致命的だと言って良いでしょう。

幸い、現行のブラウザーは先述の短いDOCTYPEを書くだけできちんと仕様に基づいてレンダリングしてくれるようになりました。思ってもみないレンダリング結果に苦しめられるくらいなら、このソラで覚えられる15文字を必ず書くようにするべきです。


[1]: https://developer.mozilla.org/ja/docs/Quirks_Mode_and_Standards_Mode