# byteball-testnet-bulider
Generate byteball genesis unit  and run your byteball testnet (alpha version) ，the project inspired by https://github.com/eaglo/byteball-genesis and https://github.com/pmiklos/byteball-devnet 

## 1.setup witeness and hub
setup 3（or more）witeness host & 1 hub，and edit witness and hub's `node_modules/byteballcore/constants.js`
```
exports.COUNT_WITNESSES = 3;  // the number your witnesses
exports.version = '1.0test';
exports.alt = '3';

exports.GENESIS_UNIT ="";

```

## 2.get  witness_info 
run a script on every witeness host to collect the witness_info,  append the witness_info to a json array file

the script to get witness_info named `readwitenessinfo.js`


## 3.and Generate a configdata file

run  `node readwitenessinfo.js`  on every witness, and get the output json objects, and put them into a configdata file called `"bgenesis.json"` 

## 4.run GENESIS_UNIT generate script 
run GENESIS_UNIT generate script called `"bgenesis.js"`, and get the GENESIS_UNIT address, set GENESIS_UNIT properly on erver witness and hub. and run hub and witness

## 5.test and improve

the script not be tested sufficient， so if you find some bugs ， welcome notice me 

contact me ： `max@outman.com`
 
