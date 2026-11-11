# CoderDojo 3Dダンスデモの環境準備チェックリスト

このPCでは、Node.js **v24.9.0**、npm **11.6.0**、Git **2.43.0.windows.1**、Chrome、GitHub CLIを確認済みです。BlenderとOBSは標準のインストール先で確認できなかったため、別の場所に入っていれば既存のものを使ってください。

## 本人が準備する項目

- [ ] **Tripo Studio**　ご自身でサインインし、必要ならProを月払いで契約します。公式表示は月額3,200円・3,000クレジット。買い切りの追加クレジットは1,000クレジットで1,500円です。必要になった場合に限りご自身で判断し、税などを含む請求総額が5,000円以内か確認します。更新日を控え、制作時はモデルを非公開に設定します。 [Tripo Studio](https://studio.tripo3d.ai/ja)・[公式料金表](https://www.tripo3d.ai/ja/pricing)
- [ ] **既存のCodex枠**　内蔵画像生成を追加課金なしで使える状態か、ご自身で確認します。作業チャットには「既存枠で画像生成可」または「画像生成は本人対応」と伝えます。契約情報や残高の画面、認証情報、APIキーの共有は不要です。 [Codex公式料金・利用枠](https://learn.chatgpt.com/docs/pricing)
- [ ] **GitHub**　例として `coderdojo-3d-dance-demo` という非公開リポジトリを作り、URLを控えます。別案は `coderdojo-character-animation`、`illustration-to-vrm-demo`。エージェントには作成済みのURLを渡します。 [GitHubの新規作成画面](https://github.com/new)
- [ ] **ニコニコ動画**　投稿に使うアカウントでサインインし、投稿画面まで開けることを確認します。 [ニコニコの投稿画面](https://studio.nicovideo.jp/)

## Windows側の準備

- [ ] **Blender 5.2 LTS**　既存の5.2系があれば起動できることを確認します。無ければ公式配布から導入します。 [Blender 5.2 LTS](https://www.blender.org/releases/5-2/)
- [ ] **VRM Add-on for Blender**　Blenderの「Get Extensions」で `VRM format` を入れて有効にし、インポート／エクスポートにVRMが出ることを確認します。 [公式拡張](https://extensions.blender.org/add-ons/vrm/)・[導入手順](https://vrm-addon-for-blender.info/en-us/installation/)
- [ ] **Blender MCP**　Charakuru同梱の指示に合わせ、Codexが同じBlenderへ接続できるようにします。テスト用のシーンで接続と読み取りを確認します。 [Charakuru公式要件](https://github.com/nanocle/Charakuru/blob/main/README.ja.md#必要なもの)
- [ ] **Charakuru v1.1.1**　公式リリースのAssetsにある `charakuru-1.1.1-2026-11-02T09-36-05-842Z.zip` を書き込み可能なフォルダに展開します。Codex側で配布元のSHA-256を照合できます。展開先で `npm.cmd start` を実行し、Chromeで `http://127.0.0.1:8766` が開けば準備完了です。 [公式配布とSHA-256](https://github.com/nanocle/Charakuru/releases/tag/v1.1.1)・[チュートリアル](https://github.com/nanocle/Charakuru/blob/main/docs/tutorial.ja.md)
- [ ] **録画**　手持ちの録画ソフトか無料のOBS Studioで、ブラウザー画面を10秒ほど収録して確認します。動画は1080p・30fpsのMP4を目安にします。 [OBS配布](https://obsproject.com/download)・[録画ガイド](https://obsproject.com/kb/standard-recording-output-guide)

契約や規約同意の画面が出た場合は、本人が操作します。ローカルのツール確認・導入・接続確認はCodexと一緒に進められます。

## Codexに引き渡す項目

- [ ] 引き継ぎZIPを展開し、そのフォルダを新しいCodexチャットの作業フォルダとして開きます。`CODEX-PROMPT.md` の全文、作成済みGitHubリポジトリのURL、Tripo準備完了の有無、既存Codex枠で画像生成できるかを伝えます。Charakuruを展開済みならそのフォルダの場所も添えます。
- [ ] 制作中、Tripoでクレジットを消費する処理はご自身で確定します。Codexから渡される入力ファイル・設定・操作の一覧を使います。候補生成のほか、部位分割、Smart UV、再テクスチャ、リギングも対象です。押す前に画面に表示される消費量を確認し、返却ファイルを指定の場所へ渡します。通常のP2候補を頭・体各4件、各100クレジットで作ると候補生成で約800クレジットです。後工程の消費は別途確認します。 [Tripoクレジット内訳](https://www.tripo3d.ai/ja/product-doc/getting-started/pricing-credits)
- [ ] ニコニコ公開とGitHubへの保存前に、公開用の説明文と保存対象を確認できるようにします。モーションと音源の利用条件が揃わない場合は、制作プロンプトに記載した代替素材や字幕版で進めます。
