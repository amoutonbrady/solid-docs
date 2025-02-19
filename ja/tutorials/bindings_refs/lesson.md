JSX は次のように DOM 要素を作成するので、代入によって Solid の要素への参照をいつでも取得できます:

```jsx
const myDiv = <div>My Element</div>
```

しかし、要素を分割せずに 1 つの連続した JSX テンプレートにまとめることで、Solid がその作成をより最適化できるというメリットがあります。

その代わりに、Solid では `ref` 属性を使用して要素への参照を取得できます。ref は基本的には、上の例のように、DOM にアタッチされる前の作成時に発生する代入です。変数を宣言するだけで、その変数に割り当てられます。

```jsx
let myDiv;

<div ref={myDiv}>My Element</div>
```

それでは、canvas 要素への参照を取得して、アニメーションさせてみましょう:

```jsx
<canvas ref={canvas} width="256" height="256" />
```

ref は、コールバック関数の形をとることもできます。これは、要素がアタッチされるまで待つ必要がない場合など、ロジックをカプセル化するのに便利です。

```jsx
<div ref={el => /* el を使って何かする... */}>My Element</div>
```
