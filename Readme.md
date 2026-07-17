# 📖 閱讀元宇宙 (Reading Metaverse)

[English Version Below](#english-version)

一個結合 3D 虛擬空間、跨時空書信交流與任務管理的沉浸式文學體驗平台。在這裡，玩家可以擁有專屬的 3D 虛擬書房，透過閱讀與生活探索賺取積分，收集名家語錄，並解鎖豐富的房間佈置與互動影音體驗。

## ✨ 核心特色

*   🛋️ **沉浸式 3D 空間**：基於 Three.js 打造。擁有動態日夜光影變化，包含可自由佈置的虛擬書房、無盡海景的露台，以及充滿香港風情的「海濱商店街」。
*   ✉️ **跨時空書信系統**：玩家可撰寫「閱讀心得」或「生活探索」，封裝成信件寄出。系統會自動進行筆友配對，玩家可以收到他人的信件並給予回信。
*   📅 **任務與習慣養成**：內建任務日曆，結合「植物栽種」系統（需每日澆水，否則會枯萎），鼓勵玩家保持持續閱讀與探索的習慣。
*   💰 **積分與扭蛋經濟**：完成任務可獲取積分。積分可用於「扭蛋機」抽取隨機家具與當代文學碎片（名家金句），或至商店購買專屬信紙、墨水及黑膠唱片。
*   🎵 **高互動性影音體驗**：
    *   **直立式鋼琴**：可直接在網頁上彈奏的 3D 鋼琴。
    *   **黑膠唱片機**：播放玩家收集到的音樂曲目，並帶有動態歌詞與進度控制。
    *   **復古收音機**：實時串流播放「香港電台第二台 (RTHK Radio 2)」。
*   🚌 **場景探索**：擬真的交通系統。玩家需走到地下巴士站，在精準的時機按下「落車鐘」，即可搭乘雙層巴士或的士前往不同的 3D 場景。

## 🛠️ 技術棧 (Tech Stack)

*   **前端框架**：HTML5, CSS3, Vanilla JavaScript
*   **3D 引擎**：[Three.js](https://threejs.org/) (WebGL)
*   **動畫庫**：[GSAP](https://greensock.com/gsap/) (提供流暢的 UI 與鏡頭運鏡)
*   **後端與資料庫**：[Firebase](https://firebase.google.com/) (Authentication, Realtime Database)
*   **影音串流**：[HLS.js](https://github.com/video-dev/hls.js/) (解析 m3u8 電台廣播)

## 🚀 快速開始 (Installation & Setup)

1. **克隆專案**
   ```bash
   git clone https://github.com/kenchan20141/letter.git
   ```

2. **設定 Firebase**
   * 至 [Firebase Console](https://console.firebase.google.com/) 建立專案並啟用 **Authentication (Google 登入)** 與 **Realtime Database**。
   * 將你的 Firebase 設定覆寫 `index.html` 中的 `firebaseConfig` 區塊：
   ```javascript
   const firebaseConfig = {
       apiKey: "YOUR_API_KEY",
       authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
       databaseURL: "https://YOUR_PROJECT_ID.firebaseio.com",
       projectId: "YOUR_PROJECT_ID"
   };
   ```

3. **本機運行**
   由於包含模組與紋理載入，請使用本地伺服器運行（例如 VS Code 的 Live Server 擴充套件，或使用 Python/Node.js 的簡易 HTTP Server）：
   ```bash
   npx http-server .
   ```


---
<a name="english-version"></a>
# 📖 Reading Metaverse

An immersive, web-based 3D virtual space combining literary exchange, penpal letter writing, and habit-tracking task management. Players own a personal 3D study room, earn points through reading logs and life explorations, collect literary quotes, and unlock rich interactive furniture and audio-visual experiences.

## ✨ Key Features

*   🛋️ **Immersive 3D Environments**: Built with Three.js. Features dynamic day/night lighting, a customizable virtual study room, a balcony with endless ocean views, and a Hong Kong-style "Shopping Street" scene.
*   ✉️ **Penpal Letter System**: Players can write "Reading Logs" or "Life Explorations" and send them as virtual letters. The system matches penpals, allowing users to receive and reply to anonymous letters.
*   📅 **Task & Habit Tracking**: Integrated task calendar coupled with a "Plant Growing" system (plants require daily watering or they wither), encouraging consistent reading habits.
*   💰 **Economy & Gacha System**: Complete tasks to earn points. Spend points on a Gacha machine to win random furniture and literary quotes, or buy custom stationery, ink, and vinyl records at the virtual shop.
*   🎵 **Interactive Audio/Visuals**:
    *   **Playable 3D Piano**: A fully functional piano playable directly in the browser.
    *   **Vinyl Record Player**: Plays collected music tracks with dynamic scrolling lyrics.
    *   **Vintage Radio**: Live streaming of "RTHK Radio 2" (Hong Kong).
*   🚌 **Scene Exploration**: Realistic transport mechanics. Players walk to a bus stop, ring the bell at the exact right moment, and take a double-decker bus or taxi to different 3D locations.

## 🛠️ Tech Stack

*   **Frontend**: HTML5, CSS3, Vanilla JavaScript
*   **3D Engine**: [Three.js](https://threejs.org/) (WebGL)
*   **Animation**: [GSAP](https://greensock.com/gsap/) (for smooth UI and camera transitions)
*   **Backend & DB**: [Firebase](https://firebase.google.com/) (Authentication, Realtime Database)
*   **Media Streaming**: [HLS.js](https://github.com/video-dev/hls.js/) (for live radio streaming)

## 🚀 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/kenchan20141/letter.git
   ```

2. **Configure Firebase**
   * Create a project in the [Firebase Console](https://console.firebase.google.com/) and enable **Authentication (Google Sign-In)** and **Realtime Database**.
   * Replace the `firebaseConfig` block in `index.html` with your own credentials:
   ```javascript
   const firebaseConfig = {
       apiKey: "YOUR_API_KEY",
       authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
       databaseURL: "https://YOUR_PROJECT_ID.firebaseio.com",
       projectId: "YOUR_PROJECT_ID"
   };
   ```

3. **Run Locally**
   Due to texture and module loading, you must run this project on a local web server (e.g., VS Code's Live Server, or a simple Node/Python HTTP server):
   ```bash
   npx http-server .
   ```
