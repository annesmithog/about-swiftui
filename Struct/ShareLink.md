# ShareLink

リンクを共有するやつ

```swift
let google = "https://www.google.com"
ShareLink(item: URL(string: google)!)
ShareLink(item: URL(string: google)!) {
    Label("Share2", systemImage: "shared.with.you")
}
ShareLink("Share3", item: URL(string: google)!)
```

<img src="/Images/View/ShareLink1.png">
