# react-native-soap-request
Simple module for making SOAP requests with WSSecurity

### Install

```
npm install LevisLuong/react-native-soap-request --save
yarn add LevisLuong/react-native-soap-request
```

### Example Usage

```js
import SoapRequest from 'react-native-soap-request';
```

```js
const soapRequest = new SoapRequest({
  security: {
    username: 'username',
    password: 'password'
  },
  targetNamespace: 'http://soap.acme.com/2.0/soap-access-services',
  commonTypes: 'http://soap.acme.com/2.0/soap-common-types',
  requestURL: soapWebserviceURL
});

const xmlRequest = soapRequest.createRequest("LoginRequest", {
        username: "abc",
        password: "xyz"
      })

const response = await soapRequest.sendRequest();

```
