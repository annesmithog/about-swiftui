<div style="font-size: 0.8rem;">

# Viewの基本情報

## はじめてのView

```swift
struct ContentView: View {
    var body: some View {
        Text("Hello, World!")
    }
}
```

<img src="/Images/View/FirstView.png">

## Modifierの使用

```swift
struct ContentView: View {
    var body: some View {
        Text("Hello, World!").font(.title)
    }
}
```

<img src="/Images/View/UseModifier.png">

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

<img src="/Images/View/UseProperty.png">

## 他のビューを組み込む

```swift
struct ContentView: View {
    var body: some View {
        Text("Hello, This is ContentView.")
        SubView()
    }
}
```

<img src="/Images/View/UseOtherrView.png">

## onAppear

ビューが表示される前に実行するアクションを追加する

```swift
Text("Hello")
    .onAppear() { print("Helloが表示されました。") }

Text("World")
    .onAppear(perform: { print("Worldが表示されました。") })
```

## onDisappear

ビューが消えた後に実行するアクションを追加する

```swift
Text("Hello")
    .onDisappear() { print("Helloと表示されていました。") }

Text("World")
    .onDisappear(perform: { print("Worldと表示されていました。") })
```

## task

##### `func task(priority: TaskPriority, () async -> Void) -> some View`

ビューが表示される前に実行する非同期タスクを追加する

```swift
Text("Hello")
    .task(priority: .background) {
        try? await Task.sleep(for: .seconds(3))
        print("Helloの表示から3秒経ちました")
    }
```

##### `func task<T>(id: T, priority: TaskPriority, () async -> Void) -> some View`

ビューが表示される前、または指定された値が変更されたときに実行する非同期タスクを追加する

```swift
struct ContentView: View {
    @State var count: Int = 0
    var body: some View {
        VStack {
            Text(String(count))
            Button("+1") {
                count += 1
            }
        }
        .task(id: count) {
            await countUp()
        }
    }
    
    func countUp() async {
        try? await Task.sleep(for: .seconds(1))
        print("Tapped")
    }
}
```


</div>
