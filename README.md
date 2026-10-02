# 𓃥白六金柱陣列 (Wave Pin Art)

一個基於 **Three.js** 與 **WebGL** 開發的互動式 3D 數位藝術網頁應用程式。透過 160×80（共 12,800 根）具備高光澤 PBR 材質的金屬針陣列，將文字轉化為動態震波與波浪擴散效果，展現科幻感十足的立體訊息視覺。

👉 **線上即時體驗**：[https://kuochili-ops.github.io/Column-matrix/](https://kuochili-ops.github.io/Column-matrix/)

---

## 🌟 核心特色 (Key Features)

- **極致 PBR 金屬光澤**：採用物理渲染材質（`MeshStandardMaterial` / `MeshPhysicalMaterial`），具備高金屬度與低粗糙度，配合多角度光源與深邃切面陰影，大幅提升文字視覺清晰度與立體感。
- **平緩機械阻尼感（Smooth Damping）**：細整高度變化速率，使柱體升降流暢，完美契合震波與漣漪向外傳導擴散的節奏。
- **精確點擊造浪換行**：支援滑鼠與觸控 Raycaster 判定，點擊針陣任意位置即可從該觸碰點發起震波傳導，並流暢切換下一行文字。
- **大海嘯進場特效（Tsunami Arrival）**：具備一鍵發動全場巨浪掃過效果，呈現氣勢磅礴的開場與清場動畫。
- **智慧多行文字與 4×2 點陣分批**：自動解析輸入的多行文字；當單行超過 8 字時，系統會自動啟動 2 秒流暢輪播。
- **自動錄影與一鍵存檔**：點擊錄影功能會先發動大海嘯開場，隨後自動進行全文字震波輪播展演，並在播畢後自動下載高畫質 WebM 影片檔。
- **URL 網址參數分享**：可將輸入的自訂訊息編碼儲存於網址，方便直接複製並分享專屬訊息給朋友。

---

## 🛠️ 技術架構 (Tech Stack)

- **前端渲染**：HTML5 Canvas, CSS3, JavaScript (ES6+)
- **3D 引擎**：[Three.js](https://threejs.org/) (r128)
  - `InstancedMesh`：高效能渲染上萬根動態金屬細柱
  - `Raycaster`：精確點陣觸碰空間座標計算
  - `OrbitControls`：視角旋轉、縮放與平移控制
- **點陣分析**：離屏 2D Canvas 文字像素渲染與動態遮罩轉換
- **媒體錄製**：原生 `MediaRecorder API` (`video/webm;codecs=vp9`)

---

## 🚀 快速開始 (Quick Start)

本專案為純前端單頁應用程式（SPA），無需安裝任何後端套件或構建步驟：

1. **複製專案庫**：
   ```bash
   git clone [https://github.com/kuochili-ops/Column-matrix.git](https://github.com/kuochili-ops/Column-matrix.git)
