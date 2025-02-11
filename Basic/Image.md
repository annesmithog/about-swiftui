<div style="font-size: 0.8rem;">

# Image

## 基本

```swift
Image("Icon")
```

## 画面のサイズ変更

##### `.resizable` - スペースに合わせてサイズ変更

```swift
Image("Icon").resizable()
```

##### アスペクト比を保ったままリサイズし、画面全体に表示

```swift
Image("Icon")
    .resizable()
    .scaledToFit()
```

## レンダリング動作の指定

##### `.antialiased` - アンチエイリアシングの適用

```swift
Image("Icon").antialiased(true)
```

##### `.symbolRenderingMode` - レンダリングモードの設定 (多色対応等)

```swift
Image("Icon").symbolRenderingMode(.hierarchical)    // ?
Image("Icon").symbolRenderingMode(.monochrome)      // ?
Image("Icon").symbolRenderingMode(.multicolor)      // ?
Image("Icon").symbolRenderingMode(.palette)         // ?
```

##### `.renderingMode` - レンダリングするか別のモードでレンデリングするか示す

```swift
Image("Icon").renderingMode(.original)
Image("Icon").renderingMode(.template)
```

##### `.interpolation` - 品質レベルの指定

```swift
Image("Icon").interpolation(.high)      // 高品質
Image("Icon").interpolation(.low)       // 低品質
Image("Icon").interpolation(.medium)    // 中品質
Image("Icon").interpolation(.none)      // 画像データを補間しない
```

## ダイナミックレンジの指定

##### `.allowedDynamicRange` - 指定された許容ダイナミックレンジで構成された新しいイメージを返す

```swift
Image("Icon").allowedDynamicRange(.standard)        // 標準範囲
Image("Icon").allowedDynamicRange(.high)            // 無制限
Image("Icon").allowedDynamicRange(.constrainedHigh) // 拡張範囲
```

</div>
