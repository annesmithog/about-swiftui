<div style="font-size: 0.8rem;">

# textFieldStyle

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

</div>
