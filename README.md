# native-echarts

[![NPM Version](https://img.shields.io/npm/v/native-echarts.svg?style=flat)](https://www.npmjs.org/package/native-echarts)
  [![npm](https://img.shields.io/npm/dm/native-echarts.svg?style=flat)](https://www.npmjs.org/package/native-echarts)
  [![License](http://img.shields.io/npm/l/native-echarts.svg?style=flat)](https://raw.githubusercontent.com/somonus/react-native-echarts/master/LICENSE.md)
  
## install

$ npm install native-echarts --save

## Usage

The Usage is complete consistent with Echarts

component props:

* *option* (object): The option for echarts: [Documentation](http://echarts.baidu.com/option.html#title)。 
* *width* (number): The width of the chart. The default value is the outer container width. 
* *height* (number): The height of the chart. The default value is 400. 


```js
import React, { Component } from 'react';
import {
  AppRegistry,
  StyleSheet,
  Text,
  View
} from 'react-native';
import Echarts from 'native-echarts';

export default class app extends Component {
  render() {
    option = {
      xAxis: {
        type: 'category',
        data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
      },
      yAxis: {
        type: 'value'
      },
      series: [
        {
          data: [820, 932, 901, 934, 1290, 1330, 1320],
          type: 'line',
          smooth: true
        }
      ]
    };
    return (
      <Echarts option={option} height={300} />
    );
  }
}

AppRegistry.registerComponent('app', () => app);

```



##Example

*run demo*

```
cd example
npm install
npm start
```

### IOS

Open the xcode project in the ios directory and click run

screenshots：

![image](https://github.com/somonus/react-native-echarts/blob/master/example/demoIOS.png)

### Android

Open the Android project in the android directory with Android Studio and click run.

screenshots：

![image](https://github.com/somonus/react-native-echarts/blob/master/example/demoAndroid.png)

## License

native-echarts is released under the MIT license.
