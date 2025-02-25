# about-swiftui

## 参考

- [SwiftUI Document (外部) [英語]](https://developer.apple.com/documentation/swiftui)
- [Swift UIの紹介チュートリアル (外部) [英語]](https://developer.apple.com/tutorials/SwiftUI)
- [Swift UIの学習チュートリアル (外部) [英語]](https://developer.apple.com/tutorials/swiftui-concepts)
- [Swift UI サンプルアプリの探索 (外部) [英語]](https://developer.apple.com/tutorials/Sample-Apps)
- [Swift UIのアップデートについて (外部) [英語]](https://developer.apple.com/documentation/Updates/SwiftUI)

---

## 例

- [ダークモード対応](/examples/Color.md)
- [Apple Music 下タブ](/examples/AppleMusicTabView.md)
- [Apple Music アルバム画面](/examples/AppleMusicAlbum.md)
- [Apple Music クレジット画面](/examples/AppleMusicCredit.md)

---

## 基本

#### [基本](/BASIC.md)

- [View](/BASIC.md#view) - ビュー
- [Text](/BASIC.md#text) - テキスト
- [Label](/BASIC.md#label) - アイコン付きラベル
- [TextField](/BASIC.md#textfield) - ユーザー入力用フィールド
- [SecureField](/BASIC.md#securefield) - パスワード入力用フィールド

#### [ボタン](/BUTTON.md)

- [Button](/BUTTON.md#button) - ボタン

#### [リンク](/LINK.md)

- [Link](/LINK.md#link) - リンク
- [ShareLink](/LINK.md#sharelink) - 共有リンク

#### [画像](/IMAGE.md)

- [Image](/IMAGE.md#image) - 画像
- [AsyncImage](/IMAGE.md#asyncimage) - 非同期画像
- [imageScale](/IMAGE.md#imagescale) - 画像のスケールを小、中、大のいずれかに変更する
- [SF Symbolsを使う](/IMAGE.md#sf-symbolsを使う)
- [symbolEffect](/IMAGE.md#symboleffect) - SF Symbols にアニメーションをつける
- [表示サイズを変更する](/IMAGE.md#表示サイズを変更する)
- [画像の比率を保って表示する](/IMAGE.md#画像の比率を保って表示する)
- [角丸](/IMAGE.md#角丸)
- [丸](/IMAGE.md#丸)

#### [コントロール＆インジケーター](/CONTROL.md)

- [Slider](/CONTROL.md#slider) - スライダー
- [Stepper](/CONTROL.md#stepper) - ステッパー
- [Toggle](/CONTROL.md#toggle) - トグル
- [Picker](/CONTROL.md#picker) - ピッカー
- DatePicker - 日付ピッカー
- ColorPicker - カラーピッカー
- Gauge - ゲージ
- ProgressView - 進捗表示

#### [メニュー](/MENU.md)

- [Menu](/MENU.md) - メニュー
- [contextMenu](/MENU.md) - コンテキストメニュー

------------------------------------------------------

## レイアウト＆配置

#### [スタック](/STACK.md)

- [HStack](/STACK.md#hstack) - 水平に並べて表示する
- [VStack](/STACK.md#vstack) - 垂直に並べて表示する
- [ZStack](/STACK.md#zstack) - 重ねて表示する
- [Grid](/STACK.md#grid) - グリッド
- [Spacer](/STACK.md#spacer) - スペース

#### [形状](/SHAPE.md)

- [長方形](/SHAPE.md#長方形)
- [円形](/SHAPE.md#円形)

------------------------------------------------------

## スタイル＆外観

#### [アニメーション](/ANIMATION.md)

- [アニメーションの基本](/ANIMATION.md#アニメーションの基本) - animationの使い方の基本
- [open-swiftui-animations by amosgyamfi (外部)](https://github.com/amosgyamfi/open-swiftui-animations) - SwiftUIアニメーション
- [SwiftUI-Animations by Shubham0812 (外部)](https://github.com/Shubham0812/SwiftUI-Animations) - SwiftUIアニメーション
- [SwiftUI-Animation by Arvindcs (外部)](https://github.com/Arvindcs/SwiftUI-Animation) - SwiftUIアニメーション
- [SwiftUI-Animations by Inncoder (外部)](https://github.com/Inncoder/SwiftUI-Animations) - SwiftUIアニメーション

#### [テキストのスタイル](/TEXT_STYLE.md)

- [font](/TEXT_STYLE.md#font) - フォントのサイズを変更する
- [fontDesign](/TEXT_STYLE.md#fontdesign) - フォントのデザインを変更する
- [fontWeight](/TEXT_STYLE.md#fontweight) - 文字の太さを変更する
- [fontWidth](/TEXT_STYLE.md#fontwidth) - 文字幅を変更する
- [textScale](/TEXT_STYLE.md#textscale) - テキストのスケールを適用する
- [truncationMode](/TEXT_STYLE.md#truncationmode) - 長いテキストの切り捨てモードを選択する
- [allowsTightening](/TEXT_STYLE.md#allowstightening) - テキストが行内に収まるように文字間のスペースを圧縮する設定を行う
- [minimumScaleFactor](/TEXT_STYLE.md#minimumscalefactor) - フォントサイズを自動調整する
- [baselineOffset](/TEXT_STYLE.md#baselineoffset) - テキストの垂直オフセットを設定する
- [lineLimit](/TEXT_STYLE.md#linelimit) - 最大行数を設定する
- [dynamicTypeSize](/TEXT_STYLE.md#dynamictypesize) - スケーラブルなコンテンツの大きさを指定する動的タイプ サイズ
- [kerning](/TEXT_STYLE.md#kerning) - 文字間の間隔を設定する
- [tracking](/TEXT_STYLE.md#tracking) - 文字間にポイント単位のスペースを追加する
- [テキストスタイル制御](/TEXT_STYLE.md#テキストスタイル制御) - テキストスタイル制御関連

#### [透明度・表示制御](/TRANSPARENCY.md)

- [opacity](/TRANSPARENCY.md#opacity) - 透明度の変更
- [hidden](/TRANSPARENCY.md#hidden) - 表示/非表示の制御
- [disabled](/TRANSPARENCY.md#disabled) - ユーザー操作可否の変更
- [help](/TRANSPARENCY.md#help) - ヘルプテキスト

#### [UIコントロールのスタイル](/UI_CONTROL_STYLE.md)

- [buttonStyle](/UI_CONTROL_STYLE.md#buttonstyle) - Button のスタイルを変更する
- [pickerStyle](/UI_CONTROL_STYLE.md#pickerstyle) - Picker のスタイルを変更する
- [datePickerStyle](/UI_CONTROL_STYLE.md#datepickerstyle) - DatePicker のスタイルを変更する
- [menuStyle](/UI_CONTROL_STYLE.md#menustyle) - Menu のスタイルを変更する
- [toggleStyle](/UI_CONTROL_STYLE.md#togglestyle) - Toggle のスタイルを変更する
- [gaugeStyle](/UI_CONTROL_STYLE.md#gaugestyle) - Gauge のスタイルを変更する
- [progressViewStyle](/UI_CONTROL_STYLE.md#progressviewstyle) - ProgressView のスタイルを変更する
- [labelStyle](/UI_CONTROL_STYLE.md#labelstyle) - Label のスタイルを変更する
- [textFieldStyle](/UI_CONTROL_STYLE.md#textfieldstyle) - TextFieldのスタイルを変更する
- [textEditorStyle](/UI_CONTROL_STYLE.md#texteditorstyle) - TextEditor のスタイルを変更する

------------------------------------------------------

## データ管理

#### プロパティラッパー

- @State - 
- @Binding - 
- @Environment - 
- @Query - 

#### [ライフサイクル管理](/LIFECYCLE.md)

- [onAppear](/LIFECYCLE.md#onappear) - ビューが消えた後に実行するアクションを追加する
- [onDisappear](/LIFECYCLE.md#ondisappear) - ビューが表示される前に実行するアクションを追加する
- [task](/LIFECYCLE.md#task) - 非同期タスク
