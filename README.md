## Webpack
webpack_template

## ディレクトリ構成
あとでかく

## Webpack関連
- ### webpack  
- ### webpack-cli  
- ### webpack-dev-server
  └ ローカルサーバーの起動

## Sass関連
- ### css-loader  
  └ cssファイルをjs用モジュールにコンパイル
- ### sass
- ### sass-loader
  └ sassをロード
- ### postcss
- ### postcss-loader  
  ├ post cssを使ってsassをコンパイル  
  └ `autoprefixer`を使用するためいに必要(後述)
- ### autoprefixer  
  └ sassをコンパイルする際にベンダープレフィックスを自動で付与
- ### mini-css-extract-plugin  
  └ js内に内包されたcssを抽出して別ファイルとして出力

## Pug関連
- ### pug
- ### pug-loader
  └ pugをロード
- ### html-webpack-plugin  
  └ htmlファイルを生成  
- ### html-webpack-pug-plugin  
  └ pugファイルからhtmlにコンパイル

## NPMインストール
```bash
npm init -y

npm i -D webpack webpack-cli webpack-dev-server css-loader sass sass-loader postcss postcss-loader autoprefixer mini-css-extract-plugin pug pug-loader html-webpack-plugin html-webpack-pug-plugin
```

## 実行コマンド
- ### package.json
  ```json
  "scripts": {
    ...
    "start": "webpack-dev-server",
    "build": "webpack",
    "watch": "webpack --watch"
    ...
  }
  ```
- ### webpackコマンド
  ```bash
  npm run start
  # ローカルサーバーの起動

  npm run build
  # 通常コンパイル

  npm run watch
  # エントリーポイントのファイルを監視
  # 変更があればコンパイル
  ```