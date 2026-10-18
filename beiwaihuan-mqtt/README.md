# 北外環 MQTT 平日排隊時長分析

可直接部署至 GitHub Pages 的靜態網頁，不需安裝套件或建置。

## 主要結果

- 最差兩天：2026-10-13、2026-09-30；平均 18.1794 分鐘／日／偵測區。
- 最佳三個一般平日：2026-09-18、2026-09-17、2026-10-01；平均 12.9041 分鐘／日／偵測區。
- 以排隊至少3輛為門檻，平均差 5.2753 分鐘，約5分17秒（29.0%）。

最佳日期不全晚於最差日期；此為依結果挑選的情境差距，不能認定為實際措施啟用前後的因果成效。分鐘數不是每位駕駛節省的旅行時間。

## 發布

將檔案推送至 main 分支。在儲存庫 Settings → Pages → Build and deployment 選擇 GitHub Actions，執行 Deploy GitHub Pages 工作流程。實際網址以成功部署結果為準。儲存庫方案與可見性須支援 GitHub Pages。

## 本機預覽

在此目錄執行 `python -m http.server 8000`，開啟 http://localhost:8000/ 。網頁透過相對路徑載入 data.json，可用於 GitHub 專案型 Pages。

## 檔案

- index.html：版面與互動。
- data.json：29個一般平日及9個偵測區的彙整資料。
- .github/workflows/pages.yml：GitHub Pages 部署流程。

本儲存庫不含原始 MQTT 日誌或來源服務憑證。
