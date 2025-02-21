# リンク

#### Link

```swift
let google = "https://www.google.com"
Link("Google", destination: URL(string: google)!)
```

<img src="/images/link/link1.png">

#### ShareLink

リンクを共有するやつ

```swift
let google = "https://www.google.com"
ShareLink(item: URL(string: google)!)
ShareLink(item: URL(string: google)!) {
    Label("Share2", systemImage: "shared.with.you")
}
ShareLink("Share3", item: URL(string: google)!)
```

<img src="/images/link/sharelink1.png">
