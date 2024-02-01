# 2024-vue-專案模板

為了熟悉環境的建立過程，簡單紀錄 vue vite 建立專案的流程。

本專案環境參考六角學院提供的 [Vue 樣板（Airbnb）](https://github.com/hexschool/vite-template/tree/airbnb)，其中有依本地端的狀況，調整了少許設定。

## 建立流程

### 一、First Commit

1. `npm create vue@latest`建立項目。
2. 安裝 [gh-pages 套件](https://www.npmjs.com/package/gh-pages)。
3. `package.json`新增部屬指令`"deploy": "vite build && gh-pages -d dist"`。
4. `vite.config.js`設定編譯路徑`base: '/<REPOSITORY_NAME>/'。
5. `src/router/index.js`更改路由歷史模式為 Hash。
6. 設置環境變數。

### 二、基本套件安裝

1. Axios：[axios、vue-axios](https://www.npmjs.com/package/vue-axios#in-vue-3)
2. Bootstrap：[下載](https://getbootstrap.com/docs/5.0/getting-started/download/#npm)、[自定義](https://getbootstrap.com/docs/5.0/customize/sass/#importing)
3. sass：`npm add -D sass`
4. 額外引入 ESLint Airbnb：參考[如何替 Vue Vite 專案加上 ESLint？](https://israynotarray.com/vue/20221002/584344963/#%E5%AE%89%E8%A3%9D-ESLint-Airbnb)

   - eslint-config-airbnb-base：規範本身
   - eslint-import-resolver-alias：解析`@`
   - eslint-plugin-import：import 規範
   - vite-plugin-eslint：警告畫面

   :pen 備註：額外安裝[eslint-plugin-prettier](https://www.npmjs.com/package/eslint-plugin-prettier#installation)，並在`.eslintrc.cjs`的`extends`陣列最後一位新增`'prettier'`。

### 三、常用套件安裝（可選）

1. vee-validate：
   - [vee-validate](https://vee-validate.logaretm.com/v4/tutorials/basics/)
   - [@vee-validate/rules](https://www.npmjs.com/package/@vee-validate/rules)
   - [@vee-validate/i18n](https://www.npmjs.com/package/@vee-validate/i18n)
2. [vue-loading-overlay](https://www.npmjs.com/package/vue-loading-overlay)
3. Swiper：[官方文件](https://swiperjs.com/vue#usage)、[六角教學文件（付範例程式碼）](https://hackmd.io/@hexschool/HkR7ttC2i?utm_source=preview-mode&utm_medium=rec)，Vue.js Components 方式（官方建議改用 　 Swiper Element）
   :error 注意引入檔案路徑，會依開發環境而不同。
4. SweetAlert2：[vue-sweetalert2](https://github.com/avil13/vue-sweetalert2)
5. AOS：[六角教學文件](https://hackmd.io/@hexschool/BJipmEnCs?utm_source=preview-mode&utm_medium=rec#Vue3AOS-%E7%AF%84%E4%BE%8B%E8%A8%AD%E8%A8%88)，在根元件匯入。
