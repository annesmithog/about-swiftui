<div style="font-size: 0.8rem;">

# progressViewStyle

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

</div>
