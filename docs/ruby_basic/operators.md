# operators (演算子)

## 1. 算術演算子(arithmetic operator)
(`+`, `-`, `*`, `/`, `%`, `*`)

## 2. ビット演算子(Bitwise operator)
(`~`, `&`, `|`, `^`, `<<`, `>>`, `[]`)

## 3. 論理演算子(Logical operator)
(`!`, `&&`, `||`, `not`, `and`, `or`)

## 4. 三項演算子(Ternary operator)
(`? :`)

例
```
a = 0
b = 2
result = a == 0 ? a + 1 : b

result #=> 1
```

## 5. 代入演算子(Assignment operator)
(`=`, `+=`, `-=`, `*=`, `/=`, `%=`, `**=`, `&=`, `|=`, `^=`, `<<=`, `>>=`)

## 6. 比較演算子(Comparison operator)
(`==`, `!=`, `<`, `>`, `<=`, `>=`, `<=>`, `===`)

＊　== と　=== の違い

|    |     演算子     |  使用場面  |
|----------|:-------------:|------:|
| == |  等価演算子(equality operator) | 同値性のチェック |
| === |   厳密等価演算子(strict equality operator) |   case式 |

`==`
```
# Numeric
5 == 5            #=> true
5 == 5.0          #=> true

## String
'a' == 'a'        #=> true
'a' == 'A'        #=> false

など、

```

`===`
```
# Numeric, String, Integer
・`==` と同じ動作


# Range
・右辺のオブジェクトが左辺に含まれるならばtrue．

例
(1..10) === 5             # true
('a'..'f') === "z"        # false


# Regexp
・右辺とマッチするかどうかを取れる
・右辺のStringが左辺の正規表現にマッチすればtrue．

例
/[0-9]{3}/ === "hello123" # true
/[0-9]{3}/ === "hello"    # false


# Module
・右辺がそのクラスのインスタンスであるかどうかを比較する
・右辺のオブジェクトが左辺のクラスかそのサブクラスのインスタンスならばtrue．

例
String === "hello"        # true
String === 1              # false

```

## 7. 範囲演算子(Range operator)
(`..`, `...`)

例
```
(1..10)   #=> 1から10まで(最後も含む)
(1...10)  #=> 1から9まで(最後を含まない)
```

参考 <br>
https://www.javatpoint.com/ruby-operators
https://www.tohoho-web.com/ruby/operators.html
https://mickey24.hatenablog.com/entry/20100910/1284052782
