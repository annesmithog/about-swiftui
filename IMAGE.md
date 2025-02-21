# 画像

#### Image

```swift
Image("Fish")
    .resizable()
    .aspectRatio(contentMode: .fit)
Text("This is fish.")
```

<img src="/images/image/image1.png">

#### AsyncImage

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

<img src="/images/image/imageasync1.png">

#### imageScale

```swift
Image(systemName: "flame").imageScale(.small)
Image(systemName: "flame").imageScale(.medium)
Image(systemName: "flame").imageScale(.large)
```

#### symbolEffect

```swift
VStack {
    Image(systemName: "flame")
    Image(systemName: "flame")
}
.font(.system(size: 60))
.symbolEffect(.bounce)
```

#### SF Symbolsを使う

```swift
HStack {
    Image(systemName: "calendar.badge.plus")
    Text("Calendar")
}
```

<img src="/images/image/sf.png">

#### 表示サイズを変更する

```swift
Image("Fish")
    .resizable()
    .frame(width: 100, height: 100)
```

<img src="/images/image/resizable.png">

#### 画像の比率を保って表示する

```swift
Image("Train")
    .resizable()
    .scaledToFit()
    .frame(width: 200, height: 200)
```

<img src="/images/image/fit.png">

#### 角丸

```swift
Image("Fish")
    .resizable()
    .scaledToFit()
    .frame(width: 300)
    .cornerRadius(50)
```

<img src="/images/image/cornerradius.png">

#### 丸

```swift
Image("Fish")
    .resizable()
    .scaledToFit()
    .frame(width: 300)
    .clipShape(Circle())
```

<img src="/images/image/circle.png">

