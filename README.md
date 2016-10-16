# Plantower sensor library for node

## Install

```javascript
npm install --save plantower
```

## How to use

```javascript
const PlantowerGx = require('./plantower');

let plantower = new PlantowerGx('PMS5003S', '/dev/ttyS0');

plantower.read().then(console.log.bind(console)).catch(err => {
    console.error('error when read data, err=' + err);
});
```

## Sensor data example

```
{
    concentration_pm1.0_normal: 0,
    concentration_pm2.5_normal: 0,
    concentration_pm10_normal: 0,
    concentration_pm1.0_atmos: 0,
    concentration_pm2.5_atmos: 0,
    concentration_pm10_atmos: 0,
    count_pm_0.3: 0,
    count_pm_0.5: 0,
    count_pm_1.0: 0,
    count_pm_2.5: 0,
    count_pm_5: 0,
    count_pm_10: 0,
    formaldehyde: 0, // only in PMS5003S
    version: 0, // not in PMS5003S
    erro: 0 // not in PMS5003S
}
```

## Supported Device Models

* PMS5001
* PMS5002
* PMS5003
* PMS5003S

## License

ISC
