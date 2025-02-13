<div style="font-size: 0.8rem;">

# datePickerStyle

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

</div>
