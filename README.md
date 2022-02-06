# Renogy BT-1
Library to read Renogy RS232 compatible BT-1 bluetooth adapter. Tested with `Rover 40A` controller and `Raspberry Pi Zero 2 W`. It might also work with other  "SRNE like" devices ie., RichSolar, PowMr, WEIZE etc.

## Example

```
pyhton3 ./example.py
```
Make sure to update mac_address and alias in `example.py`.

**How to get mac address?**

Use any BLE scanner apps like [BLEScanner](https://play.google.com/store/apps/details?id=com.macdom.ble.blescanner) and look for devices with alias `BT-TH-XXXX`.

**Output**

```
INFO:root:Adapter status - Powered: True
INFO:root:Starting discovery...
INFO:root:Devices found: 5
INFO:root:Found bt1 device BT-TH-B00FXXXX  [XX:6F:B0:0F:XX:XX]
INFO:root:[80:6f:b0:0f:ea:2b] Discovered, alias = BT-TH-B00FXXXX
INFO:root:[80:6F:B0:0F:EA:2B] Connected
INFO:root:[80:6f:b0:0f:ea:2b] Discovered, alias = BT-TH-B00FXXXX
INFO:root:[80:6f:b0:0f:ea:2b] Discovered, alias = BT-TH-B00FXXXX
INFO:root:[80:6F:B0:0F:EA:2B] Resolved services
INFO:root:subscribed to notification 0000fff1-0000-1000-8000-00805f9b34fb
INFO:root:found write characteristic 0000ffd1-0000-1000-8000-00805f9b34fb
INFO:root:resolved services
DEBUG:root:create_read_request 256 => [255, 3, 1, 0, 0, 30, 209, 224]
INFO:root:characteristic_enable_notifications_succeeded
INFO:root:characteristic_enable_notifications_succeeded
DEBUG:root:{'battery_percentage': 100, 'battery_voltage': 14.4, 'controller_temperature': 37, 'battery_temperature': 25, 'load_voltage': 14.4, 'load_current': 1.3, 'load_power': 1, 'pv_voltage': 19.2, 'pv_current': 5.26, 'pv_power': 101, 'max_charging_power_today': 276, 'max_discharging_power_today': 6, 'charging_amp_hours_today': 59, 'discharging_amp_hours_today': 2, 'power_generation_today': 797, 'power_generation_total': 10960}
INFO:root:Gracefully exit: Disconnecting device: BT-TH-B00FXXXX [80:6F:B0:0F:XX:XX]
```

## Dependencies

```
gatt
libscrc
```
