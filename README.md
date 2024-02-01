# 2024-vue-專案模板

為了熟悉環境的建立過程，簡單紀錄 vue vite 建立專案的流程。

本專案環境參考六角學院提供的 [Vue 樣板（Airbnb）](https://github.com/hexschool/vite-template/tree/airbnb)，其中有依本地端編輯器的狀況，調整了少許設定。

## 建立流程

### 一、建立與部屬

1. `npm create vue@latest`建立項目。
2. 安裝 [gh-pages 套件](https://www.npmjs.com/package/gh-pages)。
3. `package.json`新增部屬指令`"deploy": "vite build && gh-pages -d dist"`。
4. `vite.config.js`設定編譯路徑`base: '/<REPOSITORY_NAME>/'。
5. `src/router/index.js`更改路由歷史模式為 Hash。
6. 設置環境變數。

### 二、基本套件安裝

1. Axios
2. sass
3. Bootstrap
4. ESLint Airbnb

### 三、常用套件安裝（可選）

1. vee-validate
2. vue-loading-overlay
3. Swiper
4. SweetAlert2
5. AOS
