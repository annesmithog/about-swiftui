<div style="font-size: 0.8rem;">

# gaugeStyle

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

</div>
