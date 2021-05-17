# react-github-page

https://akiyoshi-takazwa.github.io/react-github-page/

## purpose

github pageを用いた公開 の練習

## github pageを用いた公開手順

公式docs
git : https://docs.github.com/ja/github/working-with-github-pages/creating-a-github-pages-site
react : https://create-react-app.dev/docs/deployment/#github-pages 

### gh-pages のインストール
`yarn add -D gh-pages`

### package.jsonの更新を確認
```
  "devDependencies": {
     "gh-pages": "^3.1.0"
   }
```

### package.jsonにhomepageを追加

username => github アカウント名
app-name => リポジトリ名

```
   "name": "hooks-snake-game",
   "version": "0.1.0",
   "private": true,
   "homepage": "https://username.github.io/app-name",
```

### scripts に　predeploy と deployを追加する

```
 "scripts": {
     "start": "react-scripts start",
     "build": "react-scripts build",
     "test": "react-scripts test",
     "eject": "react-scripts eject"
     "eject": "react-scripts eject",
     "predeploy": "yarn run build",
     "deploy": "gh-pages -d build"
   },

```

### デプロイ

`yarn run deploy`


### リポジトリのsettings のpagesから テーマなど設定可能


## localhost への接続

git clone 後、`yarn start`

http://localhost:3000
