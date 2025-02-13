<div style="font-size: 0.8rem;">

# View

## はじめてのView

```swift
struct ContentView: View {
    var body: some View {
        Text("Hello, World!")
    }
}
```

<img src="/Images/View/View1.png">

## Modifierの使用

```swift
struct ContentView: View {
    var body: some View {
        Text("Hello, World!")
            .font(.title)
    }
}
```

<img src="/Images/View/View2.png">

## プロパティの使用

```swift
struct ContentView: View {
    let mainFont: Font = .largeTitle
        
    var body: some View {
        VStack {
            Text("Hello, World!").font(mainFont)
            Text("Hello, World.")
        }
    }
}
```

<img src="/Images/View/View3.png">

## 他のビューを組み込む

```swift
struct ContentView: View {
    var body: some View {
        Text("Hello, This is ContentView.")
        SubView()
    }
}
```

<img src="/Images/View/View4.png">

</div>
