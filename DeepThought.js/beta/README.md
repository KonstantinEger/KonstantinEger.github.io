# Getting Started

> HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <title>DeepThought.js</title>
    <script src="https://lavakonsti.../.../DeepThought.min.js" charset="utf-8"></script>
    <script src="./app.js"></script>
  </head>
  <body>
  </body>
</html>
```

> JavaScript:

```javascript
// initialize the neural network
let nn = new dt.NeuralNetwork();

// init and add the layers
let layers = [
  { type: 'input', nodes: 2 },
  { type: 'hidden', nodes: 4},   // NOTE: order of the hidden layers is important
  { type: 'hidden', nodes: 4},
  { type: 'output', nodes: 2}
];

nn.addLayers(layers);

// train the neural network
// IMPORTANT: Work In Progress
nn.train([trainingData], [targetData], (errorRate) => {
  console.log(errorRate);

  use();
}, iterations?); // NOTE: default is 10000

function use() {
  let result = nn.predict([someData]);
}
```
