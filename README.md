# Habpanel / Xiaomi Humidity Temperature Pressure sensor 
Widget designed for 2x2 habpanel dashboard grid <br>
<b>Note:</b> Use 100% of browser zoom
<hr>
<b>*.things</b> file:<br>
<code>
Thing mihome:sensor_weather_v1:YOUR ID "Xiaomi Temperature Sensor" [itemId="YOUR ID"]
</code>

<b>*.items</b> file:<br>
<code>
//Xiaomi Temperature and Humidity Sensor<br>
Number HT_Temperature "Temperatire" <temperature> { channel="mihome:sensor_weather_v1:YOUR ID:temperature" }<br>
Number HT_Humidity "Humidity" <humidity> { channel="mihome:sensor_weather_v1:YOUR ID:humidity" }<br>
Number HT_Pressure "Pressure"  { channel="mihome:sensor_weather_v1:YOUR ID:pressure" }<br>
Number HT_Battery "Battery" <battery> { channel="mihome:sensor_weather_v1:YOUR ID:batteryLevel" }<br>
Switch HT_BatteryLow "Battery Low" <energy> { channel="mihome:sensor_weather_v1:YOUR ID:lowBattery" }<br>
</code>


![Alt text](https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/device.jpg "Device")

![Alt text](https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/widget_view1.png "Dashboard view")

![Settings view image](https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/widget_settings1.png?raw=true "Settings view")