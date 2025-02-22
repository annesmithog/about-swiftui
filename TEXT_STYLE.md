# テキストのスタイル

#### font

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

<img src="/images/text_style/Font.png">

#### fontDesign

```swift
Text("Text 1").fontDesign(.default)
Text("Text 2").fontDesign(.monospaced)
Text("Text 3").fontDesign(.rounded)
Text("Text 4").fontDesign(.serif)
```

<img src="/images/text_style/FontDesign.png">

#### fontWeight

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

<img src="/images/text_style/FontWeight.png">

#### fontWidth

```swift
Text("Text 1").fontWidth(.compressed)
Text("Text 2").fontWidth(.condensed)
Text("Text 3").fontWidth(.expanded)
Text("Text 4").fontWidth(.standard)
```

<img src="/images/text_style/FontWidth.png">

#### textScale

```swift
Text("Text 1").textScale(.default)
Text("Text 2").textScale(.secondary)
```

#### truncationMode

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

<img src="/images/text_style/TruncationMode.png">

#### allowsTightening

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

<img src="/images/text_style/AllowsTightening.png">

#### minimumScaleFactor

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

<img src="/images/text_style/MinimumScaleFactor.png">

#### baselineOffset

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

<img src="/images/text_style/BaselineOffset.png">

#### lineLimit

```swift
Text("Self care, I'm treatin' me right, yeah. Hell yeah, we gonna be alright")
    .lineLimit(1)
```

#### dynamicTypeSize

```swift
Text("Text 1").dynamicTypeSize(.accessibility1)
```

#### kerning

```swift
Text("I just need a way out of my head")
Text("I just need a way out of my head").kerning(3)
```

#### tracking

```swift
Text("I just need a way out of my head")
Text("I just need a way out of my head").tracking(3)
```

#### テキストスタイル制御

```swift
Text("Text A").bold()
Text("Text B").italic()
Text("Text C").underline()
Text("Text D").strikethrough()
Text("Text E").textCase(.lowercase)
Text("Text 1234").monospaced()
Text("Text 5678").monospacedDigit()
```

<img src="/images/text_style/TextStyle.png">
