# コントロール＆インジケーター

#### Slider

```swift
@State private var score: Double = 6.0
@State private var isEditing: Bool = false
var body: some View {
    VStack {
        Slider(
            value: $score,
            in: 0...10,
            step: 0.1,
            onEditingChanged: { editing in
                isEditing = editing
            }
        )
        Text("\(score)").foregroundColor(isEditing ? .red : .blue)
    }
}
```

<img src="/images/control/slider.png">

#### Stepper

```swift
@State private var value: Int = 0
let step = 1
let range = 0...100
var body: some View {
    Stepper(
        value: $value,
        in: range,
        step: step
    ) {
        Text("Value: \(value) [\(range.description)]")
    }
    .padding(10)
}
```

<img src="/images/control/stepper.png">

#### Toggle

```swift
@State private var isOn = false
var body: some View {
    
    Toggle(isOn: $isOn) {
        Text("Toggle 1")
    }
    
    Toggle(
        "Toggle 2",
        systemImage: "person",
        isOn: $isOn
    )
    
    Toggle("Toggle 3", isOn: $isOn)
    
    Toggle(isOn: $isOn) {
        Text("Toggle 4-1")
        Text("Toggle 4-2")
    }
    
    Toggle("Toggle 5", isOn: $isOn).toggleStyle(.button)
}
```

<img src="/images/control/toggle.png">

#### Picker

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

<img src="/images/control/picker.png">

