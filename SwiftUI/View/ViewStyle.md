<div style="font-size: 0.8rem;">

# Viewのスタイル

## `buttonStyle`

```swift
Button("Sign In") {}.buttonStyle(.bordered)
```

<img src="/Images/View/ButtonStyle.png">

## `pickerStyle`

Pickerのスタイルを変更する

OSによっても表示が異なる。FormやSectionで囲んで使用することもある。

```swift
Picker("Dir", selection: $pickerIndex) {
    Text("L").tag(0)
    Text("R").tag(1)
}
.pickerStyle(.automatic)
```

##### `.automatic`

<img src="/Images/View/PickerStyleAutomatic.png">

##### `.inline`

<img src="/Images/View/PickerStyleInline.png">

##### `.segmented`

<img src="/Images/View/PickerStyleSegmented.png">

##### `.wheel`

省略

##### `.menu`

省略

##### `.radioGroup`

省略

## `datePickerStyle`

DatePickerのスタイルを変更する

```swift
@State var date = Date()
var body: some View {
    DatePicker(
        "Start Date",
        selection: $date,
        displayedComponents: [.date]
    )
    .datePickerStyle(.automatic)
}
```

##### `.compact`

<img src="/Images/View/DatePickeCompact.png">

##### `.graphical`

<img src="/Images/View/DatePickerGraphical.png">

##### `.wheel`

<img src="/Images/View/DatePickerWheel.png">

## `menuStyle`

Menuのスタイルを変更する

```swift
Menu("性別") {
    Button("男") {}
    Button("女") {}
}
.menuStyle(.button)
```

<img src="/Images/View/MenuStyleButton.png">

## `toggleStyle`

Toggleのスタイルを変更する

```swift
@State var useBluetooth = false
var body: some View {
    Toggle("Bluetooth", isOn: $useBluetooth)
        .toggleStyle(.button)
}
```

##### `.button`

<img src="/Images/View/ToggleStyleButton.png">

##### `.switch`

<img src="/Images/View/ToggleStyleSwitch.png">

## `gaugeStyle`

Gaugeのスタイルを変更する

```swift
@State var hp: Double = 40.0
var body: some View {
    Gauge(value: hp, in: 0...100) {
        Text("HP")
    }
    .gaugeStyle(.accessoryCircular)
}
```

##### `.accessoryCircular`

<img src="/Images/View/Gauge1.png">

##### `.accessoryCircularCapacity`

<img src="/Images/View/Gauge2.png">

##### `.accessoryLinear`

<img src="/Images/View/Gauge3.png">

##### `.`accessoryLinearCapacity

<img src="/Images/View/Gauge4.png">

##### `.linearCapacity`

<img src="/Images/View/Gauge5.png">

## `progressViewStyle`

ProgressViewのスタイルを変更する

```swift
@State var progress: Double = 0.7
var body: some View {
    ProgressView()
        .progressViewStyle(.circular)
    
    ProgressView(value: progress)
        .progressViewStyle(.linear)
}
```

<img src="/Images/View/ProgressView1.png">

## `labelStyle`

Labelのスタイルを変更する

```swift
VStack {
    Label("Fire", systemImage: "flame.fill")
    Label("Lightning", systemImage: "bolt.fill")
}
.labelStyle(.iconOnly)
```

##### `.iconOnly`

<img src="/Images/View/LabelStyle1.png">

##### `.titleAndIcon`

<img src="/Images/View/LabelStyle2.png">

##### `.titleOnly`

<img src="/Images/View/LabelStyle3.png">

## `textFieldStyle`

TextFieldのスタイルを変更する

```swift
@State var username: String = "@annesmith"
var body: some View {
    TextField(
        "Username",
        text: $username
    )
    .foregroundColor(.blue)
    .textFieldStyle(.plain)
}
```

##### `.plain`

<img src="/Images/View/TextField1.png">

##### `.roundedBorder`

<img src="/Images/View/TextField2.png">

## `textEditorStyle`

TextEditorのスタイルを変更する

```swift
@State var $line: String = "@annesmith"
var body: some View {
    TextEditor(text: $line)
        .textEditorStyle(.plain)
}
```

<img src="/Images/View/TextEditor1.png">

---

</div>
