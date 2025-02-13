# truncationMode

```swift
VStack {
Text("I'm always say I want change but I ain't same.")
    .foregroundColor(.red)
    .frame(width: 150, height: 60)
    .truncationMode(.head)
Text("I'm always say I want change but I ain't same.")
    .frame(width: 150, height: 60)
    .foregroundColor(.blue)
    .truncationMode(.middle)
Text("I'm always say I want change but I ain't same.")
    .frame(width: 150, height: 60)
    .foregroundColor(.green)
    .truncationMode(.tail)
}
```

<img src="/Images/View/TruncationMode.png">
