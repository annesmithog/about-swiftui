# Apple Music 下タブ

```swift
TabView {
    HomeView()
        .tabItem {
            Label("ホーム", systemImage: "house.fill")
        }
    HomeView()
        .tabItem {
            Label("新着", systemImage: "square.grid.2x2.fill")
        }
    HomeView()
        .tabItem {
            Label("ラジオ", systemImage: "dot.radiowaves.left.and.right")
        }
    HomeView()
        .tabItem {
            Label("ライブラリ", systemImage: "music.quarternote.3")
        }
    HomeView()
        .tabItem {
            Label("検索", systemImage: "magnifyingglass")
        }
}
```

<img src="/images/examples/apple_music/AppleMusicTabView.png">
