<div style="font-size: 0.8rem;">

# コントロールとインジケーター

## はじめてのButton

```swift
// 基本
Button(action: { print("Button 1 clicked") }) {
    Text("Button 1")
}
// Label使用 1
Button(action: {} ) {
    Label("Button 2", systemImage: "person.fill")
}
// Label使用 2
Button("Button 3", systemImage: "person", action: {} )
// labelStyle適用
Button("Button 4", systemImage: "flame", action: {} )
    .labelStyle(.iconOnly)
// 役割の割り当て
Button("Button 5", role: .destructive, action: {})
// スタイル設定
Button("Sign In", action: {}).buttonStyle(.borderedProminent)
Button("Register", action: {}).buttonStyle(.bordered)
```

[Button Style](/SwiftUI/View/ViewStyle.md#buttonstyle)

<img src="/Images/View/Button1.png">

## はじめてのLink

```swift
let google = "https://www.google.com"
Link("Google", destination: URL(string: google)!)
```

<img src="/Images/View/Link1.png">

## はじめてのShareLink

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

## Slider

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

<img src="/Images/View/Slider1.png">

## Stepper

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

<img src="/Images/View/Stepper1.png">

## Toggle

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

[Toggle Style](/SwiftUI/View/ViewStyle.md#togglestyle)

<img src="/Images/View/Toggle1.png">

## Picker

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

[Picker Style](/SwiftUI/View/ViewStyle.md#pickerstyle)

<img src="/Images/View/Picker1.png">

## DatePicker

Pickerの日付版。省略。

[DatePicker Style](/SwiftUI/View/ViewStyle.md#datepickerstyle)


## ColorPicker

Pickerの色版。省略。

## Gauge

範囲内の値を表示する

[Gauge Style](/SwiftUI/View/ViewStyle.md#gaugestyle)

## ProgressView

タスク完了までの進行状況を表示する

[ProgressView Style](/SwiftUI/View/ViewStyle.md#progressviewstyle)

</div>
