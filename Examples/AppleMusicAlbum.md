# Apple Music アルバム

```swift
// 曲情報モデル
struct Song {
    let title: String
    let isExplicit: Bool
}

let songList = [
    Song(title: "Come Back to Earth", isExplicit: false),
    Song(title: "Hurt Feelings", isExplicit: true),
    Song(title: "What's the Use?", isExplicit: true),
    Song(title: "Perfecto", isExplicit: true),
    Song(title: "Self Care", isExplicit: true),
    Song(title: "Wings", isExplicit: true),
    Song(title: "Ladders", isExplicit: true),
    Song(title: "Small Worlds", isExplicit: true),
    Song(title: "Conversation, Pt. 1", isExplicit: true),
    Song(title: "Dunno", isExplicit: true),
    Song(title: "Jet Fuel", isExplicit: true),
    Song(title: "2009", isExplicit: true),
    Song(title: "So It Goes", isExplicit: true),
]

// アルバムカバーView
struct AlbumCover: View {
    let albumCover: Image
    let albumName: String
    let singerName: String
    let releaseYear: Int
    
    var body: some View {
        ZStack(alignment: .bottom) {
            albumCover.resizable()
                .scaledToFit()
                .padding()
            
            VStack {
                VStack(spacing: 5) {
                    Text(albumName)
                        .font(.headline)
                        .bold()
                    Text(singerName)
                        .font(.subheadline)
                    Text(String(releaseYear))
                        .font(.caption)
                        .foregroundColor(.secondary)
                }
                .frame(maxWidth: .infinity)
                .padding(.bottom, 5)
                .background {
                    Color
                        .black
                        .blur(radius: 50, opaque: false)
                        .opacity(0.5)
                }
            }
        }
    }
}

// ボタンView
struct SoundButton: View {
    let text: String
    let systemImage: String
    
    var body: some View {
        Button(action: {}) {
            Label(text, systemImage: systemImage)
                .font(.system(size: 16))
                .bold()
                .foregroundColor(.black)
                .frame(maxWidth: .infinity)
                .padding(.vertical, 10)
                .background(.gray.opacity(0.5))
                .cornerRadius(10)
        }
    }
}

// 曲View
struct SongRow: View {
    let index: Int
    let song: Song
    
    var body: some View {
        VStack {
            HStack {
                Text("\(index)")
                    .font(.caption)
                    .foregroundColor(.gray)
                    .padding(.leading, 25)
                Text(song.title)
                    .font(.caption)
                    .padding(.leading, 10)
                if song.isExplicit {
                    Text("E")
                        .font(.system(size: 9))
                        .bold()
                        .background(
                            RoundedRectangle(cornerRadius: 2)
                                .fill(.gray)
                                .frame(width: 12, height: 12)
                        )
                        .padding(.leading, 0)
                    
                }
                Spacer()
                Image(systemName: "ellipsis")
                    .padding(.trailing, 20)
                    .imageScale(.small)
            }
            .padding(.vertical, 6)
            Divider()
        }
    }
}

struct ContentView: View {
    let albumCover: Image = Image("Swimming")
    let albumName: Text = Text("Swimming")
        .font(.title)
        .fontWeight(.bold)
    let singerName: Text = Text("Mac Miller")
        .font(.subheadline)
        .foregroundStyle(.gray)
    let albumDetails: Text = Text("2018")
        .font(.caption)
        .foregroundStyle(.gray)
    var body: some View {
        ScrollView {
            VStack(spacing: 0) {
                AlbumCover(
                    albumCover: Image("Swimming"),
                    albumName: "Swimming",
                    singerName: "Mac Miller",
                    releaseYear: 2018
                )
                .background(.white)
                
                HStack {
                    SoundButton(text: "Play", systemImage: "play.fill")
                    SoundButton(text: "Shuffle", systemImage: "shuffle")
                }
                .padding()
                
                VStack {
                    ForEach(songList.indices, id: \.self) { index in
                        SongRow(index: index + 1, song: songList[index])
                    }
                }
                .padding(.vertical, 10)
            }
        }
        .edgesIgnoringSafeArea(.all)
        .foregroundColor(Color("ColorLabelText"))
        .background(Color("ColorLabel"))
    }
}
```

<img src="/images/examples/apple_music/AppleMusicAlbum.png">
