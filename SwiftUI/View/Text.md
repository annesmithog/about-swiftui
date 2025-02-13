<div style="font-size: 0.8rem;">

# テキスト

## `Text`

テキスト

```swift
Text("Hello")
```

## `Label`

タイトル付きのアイコン

```swift
Label("Lightning", systemImage: "bolt.fill")
```

## `TextField`

表示・編集できる長い形式のテキスト

```swift
@State private var username: String = ""
var body: some View {
    TextField("Username", text: $username)
}
```

## `SecureField`

編集できるプライベートなテキスト

```swift
@State private var password: String = ""
var body: some View {
    SecureField("Password", text: $password)
}
```

## `.font`

フォントの大きさを設定する

```swift
Text("Text 1").font(.largeTitle)
Text("Text 2").font(.title)
Text("Text 3").font(.title2)
Text("Text 4").font(.title3)
Text("Text 5").font(.headline)
Text("Text 6").font(.subheadline)
Text("Text 7").font(.body)
Text("Text 8").font(.callout)
Text("Text 9").font(.caption)
Text("Text 10").font(.caption2)
Text("Text 11").font(.footnote)
```

<img src="/Images/View/Font.png">

## `.fontDesign`

フォントデザインを設定する

```swift
Text("Text 1").fontDesign(.default)
Text("Text 2").fontDesign(.monospaced)
Text("Text 3").fontDesign(.rounded)
Text("Text 4").fontDesign(.serif)
```

<img src="/Images/View/FontDesign.png">

## `.fontWeight`

フォントの太さを設定する

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

<img src="/Images/View/FontWeight.png">

## `.fontWidth`

フォントの幅を設定する

```swift
Text("Text 1").fontWidth(.compressed)
Text("Text 2").fontWidth(.condensed)
Text("Text 3").fontWidth(.expanded)
Text("Text 4").fontWidth(.standard)
```

<img src="/Images/View/FontWidth.png">

## `.textScale`

テキストスケールを適用する

```swift
Text("Text 1").textScale(.default)
Text("Text 2").textScale(.secondary)
```

## `.dynamicTypeSize`

端末側で設定したサイズを設定する

```swift
Text("Text 1").dynamicTypeSize(.accessibility1)
```

## テキストスタイル制御

```swift
Text("Text A").bold()
Text("Text B").italic()
Text("Text C").underline()
Text("Text D").strikethrough()
Text("Text E").textCase(.lowercase)
Text("Text 1234").monospaced()
Text("Text 5678").monospacedDigit()
```

<img src="/Images/View/TextStyle.png">

## `.truncationMode`

長いテキストの切り捨てモードを設定する

```swift
VStack {
Text("I'm always say I want change but I ain't same.")
    .foregroundColor(.red)
    .frame(width: 150, height: 60)
    .truncationMode(.head)
Text("I'm always say I want change but I ain't same.")
    .frame(width: 150, height: 60)
    .foregroundColor(.blue)
    .truncationMode(.middle)
Text("I'm always say I want change but I ain't same.")
    .frame(width: 150, height: 60)
    .foregroundColor(.green)
    .truncationMode(.tail)
}
```

<img src="/Images/View/TruncationMode.png">

## `.allowsTightening`

行内に収まるように文字間のスペースを圧縮する

```swift
VStack {
    Text("I'm always say I want change but I ain't same.")
        .foregroundColor(.red)
        .frame(width: 210, height: 60)
        .allowsTightening(true)
        
    Text("I'm always say I want change but I ain't same.")
        .frame(width: 210, height: 60)
        .foregroundColor(.blue)
        .allowsTightening(false)
}
```

<img src="/Images/View/AllowsTightening.png">

## `.minimumScaleFactor`

スペースに収まるように縮小される最小量を設定する

```swift
HStack {
    Text("SLOW DANCING IN THE DARK - BALLADS 1")
        .lineLimit(1)
        .minimumScaleFactor(0.5)
    Text("by JOJI")
}

HStack {
    Text("SLOW DANCING IN THE DARK - BALLADS 1")
        .lineLimit(1)
    Text("by JOJI")
}
```

<img src="/Images/View/MinimumScaleFactor.png">

## `.baselineOffset`

垂直オフセットを設定する

```swift
HStack() {
    Text("High")
        .baselineOffset(10)
        .border(.red)
    Text("Middle")
        .baselineOffset(0)
        .border(.yellow)
    Text("Low")
        .baselineOffset(-10)
        .border(.green)
}
```

<img src="/Images/View/BaselineOffset.png">

## `.kerning`

文字間の間隔を設定する

```swift
Text("I just need a way out of my head")
Text("I just need a way out of my head").kerning(3)
```

## `.tracking`

文字間にポイント単位のスペースを追加する

```swift
Text("I just need a way out of my head")
Text("I just need a way out of my head").tracking(3)
```

## `.lineLimit`

行数を設定する

```swift
Text("Self care, I'm treatin' me right, yeah. Hell yeah, we gonna be alright")
    .lineLimit(1)
```

</div>
