## Graphin

![](https://camo.githubusercontent.com/2b77a87432d47fb4f20f5b0bfbdcb2db15775dab/68747470733a2f2f67772e616c697061796f626a656374732e636f6d2f6d646e2f726d735f3030656463622f616674732f696d672f412a456b4a6d52726d754a41674141414141414141414141426b4152516e4151)

[中文](./README.cn-ZH.md)

Graphin means Graph Insight (analysis of graphs). It is a library based on G6 and React and offers graph analysis toolkit out of the box. Graphin's logo is graphene, which means the potential in the future.

For more infomation, please check the [Graphin Website](https://antv.vision/graphin).

Graphin use lerna to management this repo. This repo contains the  following packages:

```bash
/packages
    graphin
    graphin-components
    graphin-studio
    graphin-site
```

Please checkout the specific package：

| Package Name             | Description                                                            |
| ------------------------ | ---------------------------------------------------------------------- |
| [@antv/graphin](https://github.com/antvis/graphin/tree/master/packages/graphin)  |    Core React component of Graphin                    |
| [@antv/graphin-components](https://github.com/antvis/graphin/tree/master/packages/graphin-components) | Graphin components                                            |
| [@antv/graphin-site](https://github.com/antvis/graphin/tree/master/packages/graphin-site)       | Graphin documentation website                                               |
| [graphin-studio](https://github.com/antvis/graphin/tree/master/packages/graphin-studio)           | A Graphin demo: generic graph analysis workbench based on Graphin |

### Graphin Quick Start

#### Install

```bash
npm run --save @antv/graphin
```

#### Usage

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Graphin, { Utils } from '@antv/graphin';

import "@antv/graphin/dist/index.css"; // 引入Graphin CSS
import './styles.css';

const App = () => {
    const data = Utils.mock(10).graphin();
    return (
        <div className="App">
            <Graphin data={data} />
        </div>
    );
};

const rootElement = document.getElementById('root');
ReactDOM.render(<App />, rootElement);
```


### Develop

-   Set npmClient

Set your npmClient in lerna.json, developers in China can set [cnpm](https://www.npmjs.com/package/cnpm)

```json
// ./lerna.json
{
    "packages": ["packages/*"],
    "npmClient": "yarn", // cnpm/npm
    "version": "0.0.0"
}
```

-   Install dependencies

```bash
npm i
```

-   Install dependencies for each package

```bash
npm run bootstrap
```

-   Start the local compilation of graphin and graphin-components

```bash
npm run start
```

> after `npm run start`

-   Start the Graphin studio demo

```bash
npm run studio
```

-   Start Graphin Doc site

```bash
npm run site
```

### More

- [Introduction to Graphin](https://graphin.antv.vision/zh/docs/manual/introduction)
- [Getting started](https://graphin.antv.vision/zh/docs/manual/getting-started)
- [API documentation](https://graphin.antv.vision/zh/docs/api/graphin)
- [GraphinStudio](https://graphin.antv.vision/zh/GraphinStudio)
