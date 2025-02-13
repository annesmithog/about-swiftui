<div style="font-size: 0.8rem;">

# 画像

## はじめてのImage

```swift
Image("Fish")
    .resizable()
    .aspectRatio(contentMode: .fit)
Text("This is fish.")
```

<img src="/Images/View/ImageEssential.png">

## SF Symbolsを使う

```swift
HStack {
    Image(systemName: "calendar.badge.plus")
    Text("Calendar")
}
```

<img src="/Images/View/ImageSFSymbols.png">

## 表示サイズを変更する

```swift
Image("Fish")
    .resizable()
    .frame(width: 100, height: 100)
```

<img src="/Images/View/ImageSize.png">

## 画像の比率を保って表示する

```swift
Image("Train")
    .resizable()
    .scaledToFit()
    .frame(width: 200, height: 200)
```

<img src="/Images/View/ImageFit.png">

## 角丸

```swift
Image("Fish")
    .resizable()
    .scaledToFit()
    .frame(width: 300)
    .cornerRadius(50)
```

<img src="/Images/View/ImageCornerRadius.png">

## 丸

```swift
Image("Fish")
    .resizable()
    .scaledToFit()
    .frame(width: 300)
    .clipShape(Circle())
```

<img src="/Images/View/ImageCircle.png">

## `.imageScale`

ビュー内の画像を小、中、大のいずれかにスケールする

```swift
Image(systemName: "flame").imageScale(.small)
Image(systemName: "flame").imageScale(.medium)
Image(systemName: "flame").imageScale(.large)
```

## `AsyncImage`

画像を非同期に読み込んで表示する

```swift
var cover = "https://img.hmv.co.jp/image/jacket/400/06/9/0/767.jpg"

AsyncImage(url: URL(string: cover)) { image in
    // 読み込まれたら色々やる
    image
        .resizable()
        .scaledToFit()
        .cornerRadius(30)
} placeholder: {
    // 読み込まれない間、ローディングアニメーション
    ProgressView()
}
.frame(width: 300, height: 300)
```

<img src="/Images/View/ImageAsync.png">

## `.symbolEffect`

Symbolにアニメーションをつける

SF Symbolsでアニメーションを確認できる

```swift
VStack {
    Image(systemName: "flame")
    Image(systemName: "flame")
}
.font(.system(size: 60))
.symbolEffect(.bounce)
```

</div>
