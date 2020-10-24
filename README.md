# vue-hello-world

## 使い方

```sh
# projectの作成。色々セットアップする。
vue create <project name>

# localhostにserve
npm run serve


```

## メモ

vue js使ってる時に気になったことをメモ

### scss使いたい時

scss使うなら以下ををダウンロード
  - `npm install sass-loader node-sass --save-dev`
  - `<style lang="scss">`を指定すればいける。

### export defaultについて

jsの機能で、指定したものを外部ファイルからimportできるようにする。
- [] ここでcomponentsの指定とか意味わからん


```js
<script>
export default {
    name: "Header",
    data() {
        return{
            msg2: "はじめまして"
        }
    }
}
</script>
```

### 子コンポーネントに値を渡すpropsの注意点と使い方

- 使い方

v-bind出なく:だけでもok.


- 注意点(参考:https://dev83.com/vue-props/)
JSのpropsに大文字を入れた場合、htmlではハイフン+小文字(ケバブケース)で表現する。
  - 子コンポーネント(Item)のJS側：`props: [discountPrice],`
  - 親コンポーネントのTemplate : `<Item discount-price="980"></Item>`


## 調べたいこと
- index.htmlがApp.vue見てる方法は？
- 

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
