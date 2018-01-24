# 「iPhoneアプリ開発講座　はじめてのSwift」

## CHAPTER06-04
- 改造してアプリ・VCのライフサイクルを確認
- #functionでコールされたメソッドをログに表示
- Xcode9.2
- シミュレータ（iOS11.2 iPhoneX）

## 結果
- 起動
    - application(_:didFinishLaunchingWithOptions)
    - loadView()
    - viewDidLoad()
    - viewWillAppear(_:)
    - viewDidAppear(_:)
    - applicationDidBecomeActive(_:)
- 表示
- ホームボタン
    - applicationWillResignActive(_:)
    - applicationDidEnterBackground(_:)
- アプリタップ
    - applicationWillEnterForeground(_:)
    - applicationDidBecomeActive(_:)

### 注意
`viewWillDisappear(_:)`と`viewDidDisappear(_:)`は、画面遷移がない場合は発火しない。

## 画面遷移がある場合
- 起動
    - application(_:didFinishLaunchingWithOptions)
    - loadView()
    - viewDidLoad()
    - viewWillAppear(_:)
    - viewDidAppear(_:)
    - applicationDidBecomeActive(_:)
- 表示
- 画面遷移
    - 次画面: loadView()
    - 次画面: viewDidLoad()
    - viewWillDisappear(_:)
    - 次画面: viewWillAppear(_:)
    - 次画面: viewDidAppear(_:)
    - viewDidDisappear(_:)