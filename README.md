# Habpanel / Xiaomi Humidity Temperature Pressure sensor 
Widget designed for 2x2 habpanel dashboard grid <br>
<b>Note:</b> Use 100% of browser zoom
<hr>

<img src="https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/widget_view1.png?raw=true" height="200">

<br>
<br>
<b>things/*.things</b> file:<br>
<pre>
Thing mihome:sensor_weather_v1:YOUR ID "Xiaomi Temperature Sensor" [itemId="YOUR ID"]
</pre>
<br>
<b>items/*.items</b> file:<br>
<pre>//Xiaomi Temperature and Humidity Sensor
Number HT_Temperature "Temperature" <temperature> { channel="mihome:sensor_weather_v1:YOUR ID:temperature" }
Number HT_Humidity "Humidity" <humidity> { channel="mihome:sensor_weather_v1:YOUR ID:humidity" }
Number HT_Pressure "Pressure"  { channel="mihome:sensor_weather_v1:YOUR ID:pressure" }
Number HT_Battery "Battery" <battery> { channel="mihome:sensor_weather_v1:YOUR ID:batteryLevel" }
Switch HT_BatteryLow "Battery Low" <energy> { channel="mihome:sensor_weather_v1:YOUR ID:lowBattery" }
</pre>
<br>
<b>sitemaps/*.sitemap</b> file:<br>
<pre>Frame label="Xiaomi Huidity Sensor" {
&nbsp;&nbsp;&nbsp;Text item=HT_Temperature label="Temperature [%.1f °C]"
&nbsp;&nbsp;&nbsp;Text item=HT_Humidity label="Humidity [%.1f %%]" icon="humidity"
&nbsp;&nbsp;&nbsp;Text item=HT_Pressure label="Pressure [%.1f kPa]" icon="pressure"
&nbsp;&nbsp;&nbsp;Text item=HT_Battery label="Battery [%s %%]"
}</pre>
<br>
<b>persistence/mysql.persist</b> file:<br>
<pre>HT_Temperature : strategy = everyChange, everyDay, restoreOnStartup
HT_Humidity : strategy = everyChange, everyDay, restoreOnStartup
HT_Pressure : strategy = everyChange, everyDay, restoreOnStartup
HT_Battery : strategy = everyChange, everyDay, restoreOnStartup</pre>



<span style="float:left;">
<img src="https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/widget_settings1.png?raw=true" height="400">
</span>
<span style="float:left;">
<img src="https://github.com/andreypopov/habpanel-widget-xiaomi-sensor_weather_v1/blob/master/readme/device.jpg?raw=true" height="400">
</span>
