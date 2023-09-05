# bpmn-expression-language

This library exports expression language that is used by from.js


## Installation

```
npm install bpmn-expression-language
```


## Usage

```javascript
npm i bpmn-expression-language

import {
  ConditionChecker
} from 'bpmn-expression-language'

const conditionChecker = new ConditionChecker(
  null,
  null
);
const result = conditionChecker.check('=list contains(["Active","Close","Dormant"], application_status.value)', {
  "PEP_check": {
      "type": "Boolean",
      "value": true,
      "valueInfo": {}
  },
  "application_status": {
      "type": "String",
      "value": "Dormant",
      "valueInfo": {}
  },
});
console.log(result) // result would be true as Dormant is there in list
```