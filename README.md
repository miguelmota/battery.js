# battery

[Battery Status API](https://developer.mozilla.org/en-US/docs/Web/API/Battery_Status_API) wrapper

# Demo

[https://lab.miguelmota.com/battery](https://lab.miguelmota.com/battery)

# Install

```bash
bower install battery
```

# Usage

```javascript
battery.on('ready', function() {
  console.log('isCharging: ' + battery.isCharging()); // true
  console.log('isDischarging: ' + battery.isDischarging()); // false
  console.log('getChargingTime: ' + battery.getChargingTime()); // 5220 (seconds)
  console.log('getDischargingTime: ' + battery.getDischargingTime()); // 0
  console.log('getLevel: ' + battery.getLevel()); // 0.54
  console.log('getPercentage: ' + battery.getPercentage()); // 54
  console.log('getStatus: ' + battery.getStatus()); // 'charging'
});

battery.on('chargingChange', function(isCharging) {
  console.log(isCharging);
});

battery.on('chargingTimeChange', function(chargingTime) {
  console.log(chargingTime);
});

battery.on('dischargingTimeChange', function(dischargingTime) {
  console.log(dischargingTime);
});

battery.on('levelChange', function(level) {
  console.log(level);
});

battery.on('error', function(error) {
  console.error(error);
});
```

# License

MIT
