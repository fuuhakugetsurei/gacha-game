# 🌌 極限抽卡模擬器 (Ultimate Gacha Simulator)

這是一個基於 HTML5、CSS3 與原生 JavaScript 開發的極限簡約風抽卡模擬器。支援多卡池自定義、複雜的保底機制判定，以及特殊的票券集點系統。

This is a minimalist Gacha Simulator built with HTML5, CSS3, and Vanilla JavaScript. It supports multiple custom pools, complex pity system logic, and a unique ticket collection system.

## ✨ 核心特色 (Core Features)

* **多卡池連動管理 (Multi-Pool Management)**：
  * 使用者可以自由新增、刪除或切換不同的召喚池。
  * Users can freely add, delete, or switch between different summoning pools.


* **進階保底與機率系統 (Advanced Pity & Probability System)**：
  * 支援自定義機率 (`@`) 與保底抽數 (`!`)。
  * Supports custom probability (`@`) and pity thresholds (`!`).
  * **改良邏輯**：低級獎勵保底不會重置總計數，只有抽中最高級獎勵 (SSR) 才會重置保底。
  * **Optimized Logic**: Low-tier pity triggers will not reset the total counter; the pity count only resets upon pulling a high-tier (SSR) reward.


* **特殊輪盤機制 (Special Wheel Mechanism)**：
  * 固定存在的特殊卡池，獎勵機率自動平均分配。
  * A fixed special pool where reward probabilities are automatically distributed equally.
  * **集點系統**：每抽到 10 個非 SSR 獎勵即可獲得一張特殊抽卡券。
  * **Ticket System**: Earn one special ticket for every 10 non-SSR rewards pulled.


* **持久化紀錄 (Data Persistence)**：
  * 透過 `localStorage` 將卡池設定與抽卡歷史儲存於瀏覽器中，重新整理也不會遺失資料。
  * All pool settings and gacha history are stored in the browser via `localStorage`, ensuring data persists after refresh.



## 🛠️ 語法說明 (Syntax Guide)

在編輯區輸入獎勵內容時，請遵循以下格式：
When entering reward content in the editor, please use the following format:

> `稀有度: 獎項名稱 @機率 !保底次數`
> `Rarity: Reward Name @Probability !PityCount`

* **範例 (Example)**: `SSR: 聖劍 @2 !80`
* 代表有 2% 機率抽中，且第 80 抽若未中則保底觸發。
* Means a 2% chance to pull, with a guaranteed drop on the 80th pull if not obtained earlier.



## 🚀 部署方式 (Deployment)

1. 將本專案的 `index.html` 上傳至 GitHub 儲存庫。
Upload the `index.html` file to your GitHub repository.
2. 在 Settings > Pages 中開啟 GitHub Pages。
Enable GitHub Pages in Settings > Pages.
3. 即可透過 `https://<你的帳號>.github.io/<專案名>/` 存取。
Access it via `https://<username>.github.io/<repo-name>/`.

---

### 💡 開發建議 (Developer's Tip)

如果你想修改介面顏色，可以調整 CSS 中的 `:root` 變數來快速更換稀有度的代表色。
If you want to customize the interface colors, you can adjust the `:root` variables in the CSS to quickly change the representative colors for each rarity.

