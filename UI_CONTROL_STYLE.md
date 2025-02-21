# UIコントロールのスタイル

#### buttonStyle

```swift
Button("Sign In") {}.buttonStyle(.bordered)
```

<img src="/images/ui_control_style/ButtonStyle.png">

#### pickerStyle

```swift
Picker("Dir", selection: $pickerIndex) {
    Text("L").tag(0)
    Text("R").tag(1)
}
.pickerStyle(.automatic)
```

###### `.automatic`

<img src="/images/ui_control_style/PickerStyleAutomatic.png">

###### `.inline`

<img src="/images/ui_control_style/PickerStyleInline.png">

###### `.segmented`

<img src="/images/ui_control_style/PickerStyleSegmented.png">

###### `.wheel`

省略

###### `.menu`

省略

###### `.radioGroup`

省略

#### datePickerStyle

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

<img src="/images/ui_control_style/DatePickeCompact.png">

##### `.graphical`

<img src="/images/ui_control_style/DatePickerGraphical.png">

##### `.wheel`

<img src="/images/ui_control_style/DatePickerWheel.png">

#### menuStyle

```swift
Menu("性別") {
    Button("男") {}
    Button("女") {}
}
.menuStyle(.button)
```

<img src="/images/ui_control_style/MenuStyleButton.png">

#### toggleStyle

```swift
@State var useBluetooth = false
var body: some View {
    Toggle("Bluetooth", isOn: $useBluetooth)
        .toggleStyle(.button)
}
```

##### `.button`

<img src="/images/ui_control_style/ToggleStyleButton.png">

##### `.switch`

<img src="/images/ui_control_style/ToggleStyleSwitch.png">

#### gaugeStyle

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

<img src="/images/ui_control_style/Gauge1.png">

##### `.accessoryCircularCapacity`

<img src="/images/ui_control_style/Gauge2.png">

##### `.accessoryLinear`

<img src="/images/ui_control_style/Gauge3.png">

##### `.accessoryLinearCapacity`

<img src="/images/ui_control_style/Gauge4.png">

##### `.linearCapacity`

<img src="/images/ui_control_style/Gauge5.png">

#### progressViewStyle

```swift
@State var progress: Double = 0.7
var body: some View {
    ProgressView()
        .progressViewStyle(.circular)
    
    ProgressView(value: progress)
        .progressViewStyle(.linear)
}
```

<img src="/images/ui_control_style/ProgressView1.png">

#### labelStyle

```swift
VStack {
    Label("Fire", systemImage: "flame.fill")
    Label("Lightning", systemImage: "bolt.fill")
}
.labelStyle(.iconOnly)
```

##### `.iconOnly`

<img src="/images/ui_control_style/LabelStyle1.png">

##### `.titleAndIcon`

<img src="/images/ui_control_style/LabelStyle2.png">

##### `.titleOnly`

<img src="/images/ui_control_style/LabelStyle3.png">

#### textFieldStyle

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

<img src="/images/ui_control_style/TextField1.png">

##### `.roundedBorder`

<img src="/images/ui_control_style/TextField2.png">

#### textEditorStyle

```swift
@State var $line: String = "@annesmith"
var body: some View {
    TextEditor(text: $line)
        .textEditorStyle(.plain)
}
```

<img src="/images/ui_control_style/TextEditor1.png">
