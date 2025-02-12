<div style="font-size: 0.8rem;">

# Viewの構成

## `opacity`

ビューの透明度を設定する

```swift
Text("Opacity 0.3").opacity(0.3)
Text("Opacity 0.7").opacity(0.6)
Text("Normal")
```

## `hidden`

ビューを非表示にする

```swift
Text("Hidden").hidden()
Text("Visible")
```

## `disabled`

ユーザーがビューを操作できるかどうか制御する

```swift
Button("A") {}.disabled(true)
Button("B") {}.disabled(false)
```

<img src="/Images/View/Disabled.png">

## `help`

```swift
Text("Tap Me")
    .help(Text("Nothing happened."))
```

</div>
