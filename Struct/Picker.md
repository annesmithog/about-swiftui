# Picker

```swift
enum Flavor: String, CaseIterable, Identifiable {
    case chocolate, vanilla, strawberry
    var id: Self { self }
}

struct ContentView: View {
    @State private var selectedFlavor: Flavor = .chocolate
    var body: some View {
        // 基本
        List {
            Picker("Flavor", selection: $selectedFlavor) {
                Text("Chocolate").tag(Flavor.chocolate)
                Text("Vanilla").tag(Flavor.vanilla)
                Text("Strawberry").tag(Flavor.strawberry)
            }
        }
        // ForEach使用、ラベル使用
        List {
            Picker(selection: $selectedFlavor) {
                ForEach(Flavor.allCases) { flavor in
                    Text(flavor.rawValue.capitalized)
                }
            } label: {
                Text("Flavor")
                Text("Choose your favorite flavor")
            }
        }
    }
}
```

<img src="/Images/View/Picker1.png">
