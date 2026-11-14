# North Shore 住宅チェック（MVP）

オークランド North Shore の購入候補の家を、地図・見学メモ・外部リンクで比較するスマホ向けWebアプリ。

## 公開方法（GitHub Pages）
1. GitHub で新しいリポジトリ（例: `northshore-house-check`）を作る
2. `index.html` をアップロード
3. Settings → Pages → Branch: `main` / `/ (root)` → Save
4. 数分後 `https://<ユーザー名>.github.io/northshore-house-check/` で開ける

## 初期設定
- 区画境界を表示するには LINZ Data Service（https://data.linz.govt.nz/）で無料APIキーを作成し、アプリの「設定」に貼り付け。
- 航空写真（任意）：LINZ Basemaps（https://basemaps.linz.govt.nz/）のAPIキー。

## データ
- すべてブラウザ内（IndexedDB）に保存。端末間で共有されません。設定画面からJSONで書き出し／読み込み。

## データ出典・方針
- 地図：© OpenStreetMap contributors／住所検索：Nominatim
- 区画：LINZ NZ Primary Parcels（CC BY 4.0、所有者名は取得しない）
- 浸水経路：Auckland Council Overland Flow Paths（参考表示）
- Homes.co.nz・NZ Police：スクレイピングせずリンクのみ
- 取得できない項目は「未確認」と表示
