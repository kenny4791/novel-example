# 給國文課同學的開發指南


## 設定環境
- 安裝 git，並[設定 ssh](http://billy3321.blogspot.tw/2009/02/github-howto.html)
- 安裝 node, npm: 在[這裡](https://nodejs.org/en/download/)選擇你的作業系統，下載並安裝。node 和 npm 會一起裝好。node是跑 Javascript 的直譯器，npm 則是一個與它搭配的套件管理工具
- 安裝 yarn：在[這裡](https://yarnpkg.com/lang/en/docs/install/#windows-tab)選擇你的作業系統，下載並安裝。yarn 是由 facebook 開發的套件管理工具，目的在讓 npm 變得效能更好

## 下載專案
- 先 fork 一份這個專案
- 改一下專案名稱
- 複製下來(記得用 ssh 版本的)：
```
# 打開你的 terminal (OSX, Linux)，或是 cmd (Windows)
# 用 cd 指令到達你的目標資料夾
git clone git@github.com:{your account}/{your repo name}.git
```  

## 安裝
```
# 一樣在你的 terminal 或 cmd
cd {your repo name} # 進到你剛剛 clone 下來的 repo 裡面
yarn
```

## 啟動
輸入底下指令，便會看到一個網頁跳出來
```
yarn start
```
這個框架使用 facebook 開發的 [`create-react-app`](https://github.com/facebookincubator/create-react-app)，有提供 Hot Reload 的功能，也就是說當你改動程式碼並儲存，畫面會自動刷新。

## 開發
請看`src/App.js`。這個框架使用的開發套件是 `React` ，一種在 Javascript 裡寫 HTML 的體系。一些基本的教學可以看[這裡](https://web-seminar.github.io/slide-v3/4/#/31?_k=sico7g)或[這裡](https://egghead.io/courses/react-fundamentals)

## 發布
開發完成後，可以使用 github 提供 GitHub Pages 的服務，簡單架設一個靜態網頁。而這個框架只要輸入以下指令：
```
yarn deploy
```
經過幾分鐘，開發好的網站就會架設在 `https://{your acount}.github.io/{your repo name}/`

## 這個框架目前提供的功能
- 一些基本 component： `Paragraph` 提供文字的區域，`MusicTrigger` 會觸發音效，等等
- 簡單多線劇情: 請參考 `src/index.js`

## 一些開發準則
- 希望達到某些效果，但還沒有相應的 component，請直接到[這裡](https://github.com/stegben/novel-example/issues) 開一個 issue 告知我，我審核後會進行開發。
- 儘管提供了一些特效，但請注意不要過度使用。簡化閱讀流程，但在必要的時候刺激你的讀者更進一步陷下去。
