<div style="font-size: 0.8rem;">

# Apple Music

## クレジット

```swift
struct ArtistRow: View {
    var name: String
    var role: String
    var body: some View {
        HStack {
            Circle()
                .fill(Color.gray.opacity(0.3))
                .frame(width: 50, height: 50)
            VStack(alignment: .leading) {
                Text(name).font(.body)
                Text(role).font(.subheadline).foregroundColor(.gray)
            }
        }
        .padding(.all, 0)
    }
}

struct ContentView: View {
    var body: some View {
        VStack(spacing: 16) {
            VStack {
                Text("Small Worlds").font(.title)
                Text("Mac Miller • Swimming • 2018").font(.subheadline)
            }
            
            List {
                Section("PERFORMING ARTISTS") {
                    ArtistRow(name: "Mac Miller", role: "Vocal")
                    ArtistRow(name: "J. Cole", role: "Programming")
                }
            }
        }
    }
}
```

<img src="/images/examples/apple_music/AppleMusicCredit.png">
