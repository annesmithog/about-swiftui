<div style="font-size: 0.8rem;">

# task

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
