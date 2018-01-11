# react-native-aztec-qrcode
A react-native component to generate [AztecCode](https://en.wikipedia.org/wiki/Aztec_Code) and [QRcode](http://en.wikipedia.org/wiki/QR_code). 

This is based on this [project](https://github.com/cssivision/react-native-qrcode)

Aztec code is one of the standars in Aviation for E-ticket generator.

## this module support iOS and Android

## Installation
```sh
npm install https://github.com/juliojlgon/react-native-aztec-qrcode
```

```sh
yarn install https://github.com/juliojlgon/react-native-aztec-qrcode
```

## Usage
```jsx
'use strict';

import React, { Component } from 'react'
import code from 'react-native-aztec-qrcode';

Aztec=code.Aztec;
QRCode=code.QRCode;

import {
    AppRegistry,
    StyleSheet,
    View,
    TextInput
} from 'react-native';

class HelloWorld extends Component {
  state = {
    text: 'react-native-azteccode-qrcode',
  };

  render() {
    return (
      <View style={styles.container}>
        <TextInput
          style={styles.input}
          onChangeText={(text) => this.setState({text: text})}
          value={this.state.text}
        />
        <QRCode
          value={this.state.text}
          size={200}
          bgColor='purple'
          fgColor='white'/>
        <Text style={styles.welcome}>
          Aztec Example
        </Text>
         <Aztec
          value={this.state.text}
          size={200}
          bgColor='black'
          fgColor='white'/>
      </View>
    );
  };
}

const styles = StyleSheet.create({
    container: {
        flex: 1,
        backgroundColor: 'white',
        alignItems: 'center',
        justifyContent: 'center'
    },
    welcome: {
        fontSize: 20,
        textAlign: 'center',
        margin: 10,
      },
    input: {
        height: 40,
        borderColor: 'gray',
        borderWidth: 1,
        margin: 10,
        borderRadius: 5,
        padding: 5,
    }
});

AppRegistry.registerComponent('HelloWorld', () => HelloWorld);

module.exports = HelloWorld;
```
## Available Props

prop      | type                 | default value
----------|----------------------|--------------
`value`   | `string`             | `http://facebook.github.io/react-native/`
`size`    | `number`             | `128`
`bgColor` | `string` (CSS color) | `"#FFFFFF"`
`fgColor` | `string` (CSS color) | `"#000000"`

<img src='qrcode.png' height = '256' width = '256'/>
<img src='azteccode.PNG' height = '256' width = '256'/>

