# NyaitterHuman

Nyaitter の年齢確認（オンデバイス推定）で使う、[@vladmandic/human](https://github.com/vladmandic/Human) 3.3.6 の Nyaitter 用カスタム配信です。

## 使い方

manifest の `nyaitter_human` にバージョンを指定し、jsDelivr 経由で読み込みます。

- 本体: `dist/human.esm.js`（上流 3.3.6 の ESM バンドル、そのまま収録）
- モデル: `models/`（本体と同じ配信元から相対で取得）

有効化する機能は顔検出（BlazeFace）と年齢推定（SSR-Net）のみです。他のモジュール（顔メッシュ・虹彩・感情・人体・手・物体・ジェスチャ等）はクライアント側の設定で無効化し、モデルも収録していません。

## 収録モデル

| ファイル | 用途 |
| --- | --- |
| `blazeface.json` / `blazeface.bin` | 顔検出 |
| `age.json` / `age.bin` | 年齢推定（SSR-Net） |
| `gender.json` / `gender.bin` | SSR-Net 有効時に上流ローダーが必須として読み込むため収録（出力は使用しません） |

## ライセンス

上流 Human の MIT ライセンスに従います（`LICENSE` を参照）。
