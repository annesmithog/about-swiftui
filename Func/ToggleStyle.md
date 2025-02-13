<div style="font-size: 0.8rem;">

# toggleStyle

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

</div>
