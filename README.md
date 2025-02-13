<div style="font-size: 0.8rem;">

# about-swiftui

## 参考

- [SwiftUI Document (外部) [英語]](https://developer.apple.com/documentation/swiftui)
- [Swift UIの紹介チュートリアル (外部) [英語]](https://developer.apple.com/tutorials/SwiftUI)
- [Swift UIの学習チュートリアル (外部) [英語]](https://developer.apple.com/tutorials/swiftui-concepts)
- [Swift UI サンプルアプリの探索 (外部) [英語]](https://developer.apple.com/tutorials/Sample-Apps)
- [Swift UIのアップデートについて (外部) [英語]](https://developer.apple.com/documentation/Updates/SwiftUI)

---

## 例

- [Apple Music](/Examples/AppleMusic.md)

---

## View

#### Basic

- struct [Text](/Struct/Text.md) - テキスト
- struct [Label](/Struct/Label.md) - タイトル付きのアイコン
- struct [TextField](/Struct/TextField.md) - 編集できるテキスト
- struct [SecureField](/Struct/SecureField.md) - 編集できるプライベートなテキスト
- protocol [View](/Protocol/View.md)
- func [onAppear](/Func/OnAppear.md) - ビューが表示される前に実行するアクションを追加する
- func [onDisappear](/Func/OnDisappear.md) - ビューが消えた後に実行するアクションを追加する
- func [task](/Func/Task.md) - ビューに実行予定の非同期タスクを追加する

#### 特性

- func [opacity](/Func/Opacity.md) - ビューの透明度を設定する
- func [hidden](/Func/Hidden.md) - ビューの表示/非表示を設定する
- func [disabled](/Func/Disabled.md) - ユーザーが操作できるか制御する
- func [help](/Func/Help.md)

#### スタイル

- func [buttonStyle](/Func/ButtonStyle.md) - Button のスタイルを変更する
- func [pickerStyle](/Func/PickerStyle.md) - Picker のスタイルを変更する
- func [datePickerStyle](/Func/DatePickerStyle.md) - DatePicker のスタイルを変更する
- func [menuStyle](/Func/MenuStyle.md) - Menu のスタイルを変更する
- func [toggleStyle](/Func/ToggleStyle.md) - Toggle のスタイルを変更する
- func [gaugeStyle](/Func/GaugeStyle.md) - Gauge のスタイルを変更する
- func [progressViewStyle](/Func/ProgressViewStyle.md) - ProgressView のスタイルを変更する
- func [labelStyle](/Func/LabelStyle.md) - Label のスタイルを変更する
- func [textFieldStyle](/Func/TextFieldStyle.md) - TextField のスタイルを変更する
- func [textEditorStyle](/Func/TextEditorStyle.md) - TextEditor のスタイルを変更する

#### アニメーション

- func [animation](/Func/Animation.md) - 状態変化に応じたアニメーションをさせる

#### テキスト関連

- func [font](/Func/Font.md) - フォントの大きさを設定する
- func [fontDesign](/Func/FontDesign.md) - フォントデザインを設定する
- func [fontWeight](/Func/FontWeight.md) - フォントの太さを設定する
- func [fontWidth](/Func/FontWidth.md) - フォントの幅を設定する
- func [textScale](/Func/TextScale.md) - テキストスケールを適用する
- func [dynamicTypeSize](/Func/DynamicTypeSize.md) - 端末側で設定したサイズを適用する
- func [テキストスタイル制御](/Func/FontTextStyle.md) - `bold`, `italic`等
- func [truncationMode](/Func/TruncationMode.md) - 長いテキストの切り捨てモードを設定する
- func [allowsTightening](/Func/AllowsTightening.md) - 行内に収まるように文字間のスペースを圧縮する
- func [minimumScaleFactor](/Func/MinimumScaleFactor.md) - スペースに収まるように縮小される最小量を設定する
- func [baselineOffset](/Func/BaselineOffset.md) - 垂直オフセットを設定する
- func [lineLimit](/Func/LineLimit.md) - 行数を設定する
- func [文字間隔の制御](/Func/Kerning.md) - `kerning`, `tracking`

#### 画像

- struct [Image](/Struct/Image.md) - 画像
- [SF Symbolsを使う](/Examples/SFSymbols.md)
- [表示サイズを変更する](/Examples/ImageResize.md)
- [画像の比率を保って表示する](/Examples/ImageScaledToFit.md)
- [角丸](/Examples/ImageCornerRadius.md)
- [丸](ImageCircle.md)
- func [imageScale](/Func/ImageScale.md) - ビュー内の画像を小、中、大のいずれかにスケールする
- struct [AsyncImage](/Struct/AsyncImage.md) - 画像を非同期に読み込んで表示する
- func [symbolEffect](/Func/SymbolEffect.md) - Symbolにアニメーションをつける

#### コントロールとインジケーター

- struct [Button](/Struct/Button.md)
- struct [Link](/Struct/Link.md)
- struct [ShareLink](/Struct/ShareLink.md)
- struct [Slider](/Struct/Slider.md)
- struct [Stepper](/Struct/Stepper.md)
- struct [Toggle](/Struct/Toggle.md)
- struct [Picker](/Struct/Picker.md)
- struct DatePicker - Pickerの日付版
- struct ColorPicker - Pickerの色版
- struct Gauge - 範囲内の値を表示する
- struct ProgressView - タスク完了までの進行状況を表示する

#### メニューとコマンド

- struct [Menu](/Struct/Menu.md)
- func [contextMenu](/Func/ContextMenu.md) - 長押ししたら出るやつ

#### 形状

- [長方形](/Examples/Rectangle.md)
- [円形](/Examples/Circle.md)

---

## レイアウト

#### Basic

- struct [HStack](/Struct/HStack.md) - サブビューを水平方向に並べる
- struct [VStack](/Struct/VStack.md) - サブビューを垂直方向に並べる
- struct [ZStack](/Struct/ZStack.md) - サブビューを重ねて並べる
- struct [Grid](/Struct/Grid.md) - 他のビューを２次元レイアウトに配置する
- struct [Spacer](/Struct/Spacer.md) - 柔軟なスペース

#### 調整

<!-- 
- func [padding](/Func/Padding.md) - padding.
- func [fixedSize](/Func/FixedSize.md) - ビューを理想的なサイズに固定する
- func [position](/Func/Position.md) - ビューの中心を親の座標空間内の指定ポイントに固定する
- func [offset](/Func/Offset.md) - 
- -->

</div>

