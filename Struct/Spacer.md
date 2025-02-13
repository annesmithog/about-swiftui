## Spacer

```swift
let name: String = "Anne Smith"
    
var body: some View {
    HStack {
        Image(systemName: "person")
        Text(name)
    }
    .border(.blue)
    
    HStack {
        Spacer()
        Image(systemName: "person")
        Text(name)
    }
    .border(.green)
    
    HStack {
        Image(systemName: "person")
        Text(name)
        Spacer()
    }
    .border(.red)
}
```

<img src="/Images/Layout/Spacer1.png">
