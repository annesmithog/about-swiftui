<div style="font-size: 0.8rem;">

# Text

## 基本

```swift
Text("Hello, World")
```

## フォント

##### `.font` - フォントの大きさ

```swift
Text("Text 1").font(.largeTitle)    // タイトル(大)
Text("Text 2").font(.title)         // タイトル
Text("Text 3").font(.title2)        // タイトル(第２階層)
Text("Text 4").font(.title3)        // タイトル(第3階層)
Text("Text 5").font(.headline)      // 見出し(大)
Text("Text 6").font(.subheadline)   // 見出し
Text("Text 7").font(.body)          // 本文
Text("Text 8").font(.callout)       // 吹き出し
Text("Text 9").font(.caption)       // キャプション
Text("Text 10").font(.caption2)     // 代替キャプション
Text("Text 11").font(.footnote)     // 注釈

// 応用
Text("Text 12").font(.system(size: 14, weight: .light, design: .serif))
```

##### `.frame` - フォントの制約

```swift
Text("Hello1 Hello2 Hello3").frame(width: 100)              // 横幅設定
Text("I don't wanna die").frame(width: 100).lineLimit(1)    // 表示1行制限
```

##### ローカライズさせない

```swift
Text(verbatim: "pencil")
```

##### `.fontWeight` - フォントの太さ

```swift
Text("Text 1").fontWeight(.black)
Text("Text 2").fontWeight(.bold)
Text("Text 3").fontWeight(.heavy)
Text("Text 4").fontWeight(.light)
Text("Text 5").fontWeight(.medium)
Text("Text 6").fontWeight(.regular)
Text("Text 7").fontWeight(.semibold)
Text("Text 8").fontWeight(.thin)
Text("Text 9").fontWeight(.ultraLight)
```

##### `.fontDesign` - フォントデザイン

```swift
Text("Text 1").fontDesign(.default)
Text("Text 2").fontDesign(.monospaced)
Text("Text 3").fontDesign(.rounded)
Text("Text 4").fontDesign(.serif)
```

##### `.fontWidth` - フォント幅

```swift
Text("Text 1").fontWidth(.compressed)   // 横にかなり狭い
Text("Text 2").fontWidth(.condensed)    // 横に狭い
Text("Text 3").fontWidth(.standard)     // 普通
Text("Text 4").fontWidth(.expanded)     // 横に広い
```

## スタイル

##### `.foregroundStyle` - テキストスタイル

```swift
Text("Text 1").foregroundStyle(.primary)    // 色がかなり濃い
Text("Text 2").foregroundStyle(.secondary)  // 色が濃い
Text("Text 3").foregroundStyle(.tertiary)   // 色が薄い
Text("Text 4").foregroundStyle(.quaternary) // 色がかなり薄い
```

##### `.bold` - 太字

```swift
Text("Text 1").bold()
```

##### `.italic` - 斜体

```swift
Text("Text 2").italic()
```

##### `.strikethrough` - 取り消し線

```swift
Text("Text 3").strikethrough()
```

##### `.underline` - 下線

```swift
Text("Text 4").underline() 
```

##### `.background` - 背景色

```swift
Text("Text").background(.pink)
```

##### `.foregroundColor` - 文字色

```swift
Text("Text").foregroundColor(.blue)
```

##### 等幅

```swift
Text("Mono12345 サンプル 1")
Text("Mono12345 サンプル 2").monospaced()       // 等幅
Text("Mono12345 サンプル 3").monospacedDigit()  // 等幅 (数値)
```

##### 幅

```swift
Text("Used to wanna be a superhero.").kerning(10)   // 文字間の幅
Text("I don't want to friends.").tracking(10)       // 字間の幅
Text("Good evening everybody.").baselineOffset(10)  // 行間の幅
```


</div>
