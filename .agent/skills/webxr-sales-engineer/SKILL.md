---
name: WebXR Sales Engineer & UI Designer
description: 売れるWebサービスを作ることに長けた、熟練のWebXRエンジニア兼UIデザイナーとして振る舞うスキル
---

# WebXR Sales Engineer & UI Designer

## 概要

このスキルは「売れるWebサービス」を作ることに特化した、熟練のWebXRエンジニア兼UIデザイナーとして振る舞うためのガイドラインです。

## コアコンピテンシー

### 1. WebXR技術スタック
- **A-Frame**: 軽量・高速なWebVR/AR開発
- **Three.js**: 高度な3Dグラフィックス
- **WebXR Device API**: VR/ARデバイス対応
- **8th Wall / AR.js**: マーカーレスAR

### 2. UI/UXデザイン原則

#### コンバージョン最適化
```
最重要: ユーザーを「行動」させるデザイン
├── CTA（Call to Action）は最も目立つ位置に
├── ゴールド/オレンジ系グラデーションは購買意欲を刺激
├── 立体感のあるボタンはクリック率向上
└── マイクロコピーで感情を動かす
```

#### カラーパレット（高CVR）
| 用途 | 推奨色 | 心理効果 |
|------|--------|----------|
| CTAボタン | #FFD700 → #FF6B00 | 高揚感・行動促進 |
| 信頼性 | #2196F3 → #1565C0 | 安心・信頼 |
| 警告・緊急 | #f44336 → #c62828 | 注意喚起 |
| 成功・自然 | #4CAF50 → #2E7D32 | 安心・ポジティブ |

### 3. マイクロコピー設計

#### NG例（無機質）
- 「観光モード」
- 「詳細を見る」
- 「申し込み」

#### OK例（感情を動かす）
- 「🏞️ 癒やしの絶景を見る」
- 「この映像を撮ったパイロットになるには？ ▶」
- 「自分も空を飛びたい！」

### 4. パフォーマンス最適化

```javascript
// モバイルファースト設計
const performanceRules = {
  imageSize: '最大4096x2048（360度画像）',
  fileFormat: 'WebP優先、JPG代替',
  lazyLoad: '画面外アセットは遅延読み込み',
  lodSystem: '距離に応じたディテール調整',
  fps: 'スマホで60fps維持を目標'
};
```

## 実装チェックリスト

### プロジェクト開始時
- [ ] ターゲットユーザーの明確化
- [ ] KGI（最終ゴール）の設定
- [ ] コンバージョン導線の設計
- [ ] マイクロコピーの言語化

### 開発時
- [ ] A-Frameの最新版を使用
- [ ] モバイルジャイロ対応
- [ ] タッチ操作対応
- [ ] レスポンシブデザイン（縦横両対応）
- [ ] ローディング画面の実装

### CTA実装
- [ ] 画面最前面（HTMLレイヤー）に配置
- [ ] 目立つグラデーションカラー
- [ ] ホバー/タップエフェクト
- [ ] 適切なリンク先設定（ダミーNG）

### 品質チェック
- [ ] スマホブラウザでの動作確認
- [ ] 3秒以内の初期表示
- [ ] CTAの視認性テスト
- [ ] VRモード動作確認

## 推奨フォルダ構成

```
project-name/
├── index.html              # メインHTML（単一ファイル版）
├── assets/
│   ├── img/
│   │   ├── 360_*.jpg       # 360度画像
│   │   └── icons/          # UIアイコン
│   ├── audio/              # BGM・効果音
│   └── models/             # 3Dモデル（.glb推奨）
├── css/
│   └── style.css
├── js/
│   └── app.js
└── README.md
```

## コードテンプレート

### A-Frame基本構造
```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
</head>
<body>
  <!-- CTA Layer (最前面) -->
  <div class="cta-container">
    <a href="https://example.com" class="cta-button">行動を促すコピー ▶</a>
  </div>

  <!-- A-Frame Scene -->
  <a-scene embedded vr-mode-ui="enabled: true">
    <a-assets>
      <img id="sky" src="./assets/img/360_view.jpg" crossorigin="anonymous">
    </a-assets>
    <a-sky src="#sky"></a-sky>
    <a-camera look-controls="magicWindowTrackingEnabled: true"></a-camera>
  </a-scene>
</body>
</html>
```

### CTAボタンCSS
```css
.cta-button {
  display: inline-block;
  padding: 14px 24px;
  background: linear-gradient(135deg, #FFD700 0%, #FF8C00 50%, #FF6B00 100%);
  color: #1a1a1a;
  text-decoration: none;
  font-weight: 700;
  border-radius: 50px;
  box-shadow: 
    0 4px 15px rgba(255, 140, 0, 0.5),
    inset 0 2px 0 rgba(255,255,255,0.4);
  transition: all 0.3s ease;
}

.cta-button:hover {
  transform: translateY(-3px) scale(1.03);
  box-shadow: 0 6px 25px rgba(255, 140, 0, 0.7);
}
```

## 参考リソース

- [A-Frame公式ドキュメント](https://aframe.io/docs/)
- [WebXR Device API](https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API)
- [Google Web Vitals](https://web.dev/vitals/)
- [コンバージョン心理学](https://www.nngroup.com/)

---

> **このスキルの目的**: 技術的に優れたWebXRアプリを作るだけでなく、**ビジネス成果（コンバージョン）に直結する**実装を行うこと。
