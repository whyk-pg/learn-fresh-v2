# Learn Fresh v2
<!-- ![Status: ToDo](https://flat.badgen.net/static/Status/ToDo/red) -->
![Status: In Progress](https://flat.badgen.net/static/Status/In%20Progress/yellow)
<!-- ![Status: Done](https://flat.badgen.net/static/Status/Done/green) -->

## 本リポジトリの目的
- Fresh v2の使い心地を確認する
- PreactのReact互換性を活用して、React資産でアプリケーションを構築する
- 内部の依存関係をnpmとJSRに絞り、esm.shの影響でできなかったlockファイルを生成できるようにする

## 本リポジトリの達成目標
- [x] Fresh v2を`jsr:@fresh/init`で作成する
- [x] esm.shを使って`react-icons`を追加し、表示する
- [ ] ~~esm.shを使って`@ark-ui/react`を追加し、表示する~~
  - React互換性の`createContext`に引っかかったらしくエラーで表示ならず([当該commit](https://github.com/whyk-pg/learn-fresh-v2/commit/65e881029e353ac17de50607fe0a4f0e43bfb51a))
- [ ] ~~`preact/compat`を使って`react-icons`を追加し、表示する~~
  - エラーにはならなかったものの、画面に表示されずDOMにも描画されていなかった([当該commit](https://github.com/whyk-pg/learn-fresh-v2/commit/1d3d5d317d8d4dda6009711e3d4abebfa1c572dd))
- [ ] HonoでAPIを構築する
- [ ] フォームを使って簡易なログイン処理を実装する

### エラー内容
#### esm.shを使った`@ark-ui/react`で発生したエラー
```sh
GET http://localhost:8000/
TypeError: Cannot read properties of undefined (reading 'context')
    at G (https://esm.sh/preact@10.25.4/denonext/hooks.mjs:2:1577)
    at n (https://esm.sh/@ark-ui/react@4.9.1/X-YXJlYWN0OnByZWFjdC9jb21wYXQKZHByZWFjdEAxMC4yNS40/denonext/dist/utils/create-context.mjs:2:363)
    at Fa (https://esm.sh/@ark-ui/react@4.9.1/X-YXJlYWN0OnByZWFjdC9jb21wYXQKZHByZWFjdEAxMC4yNS40/denonext/react.mjs:2:9389)
    at https://esm.sh/@ark-ui/react@4.9.1/X-YXJlYWN0OnByZWFjdC9jb21wYXQKZHByZWFjdEAxMC4yNS40/denonext/react.mjs:2:9617
    at Object.t (https://esm.sh/preact@10.25.4/denonext/compat.mjs:2:1860)
    at U (file:///home/windchime-yk/.cache/deno/npm/registry.npmjs.org/preact-render-to-string/6.5.13/dist/index.mjs:1:5660)
    at U (file:///home/windchime-yk/.cache/deno/npm/registry.npmjs.org/preact-render-to-string/6.5.13/dist/index.mjs:1:5330)
    at U (file:///home/windchime-yk/.cache/deno/npm/registry.npmjs.org/preact-render-to-string/6.5.13/dist/index.mjs:1:6324)
    at U (file:///home/windchime-yk/.cache/deno/npm/registry.npmjs.org/preact-render-to-string/6.5.13/dist/index.mjs:1:6324)
    at U (file:///home/windchime-yk/.cache/deno/npm/registry.npmjs.org/preact-render-to-string/6.5.13/dist/index.mjs:1:4876)
```

## 参考資料
- 特になし
