# Taco-Bell-GPS-Locator-and-Car-Gauge-
ESP32-S3 AMOLED dashboard for the 2019 F-150 2.7L EcoBoost. Features Bluetooth LE OBD-II boost, RPM, coolant and supported oil-pressure gauges, GPS speed and trip tracking, swipe navigation, and an offline Taco Bell locator with animated “TACO TIME” arrival effects. Built with Arduino and PlatformIO for VS Code.

A six-page digital dashboard built for the 2019 Ford F-150 2.7L EcoBoost using an ESP32-S3 and a 1.75-inch round AMOLED touchscreen. It reads live vehicle data through a KONNWEI KW901 Bluetooth LE OBD-II adapter and uses onboard GPS for speed, trip tracking, and an offline Taco Bell locator. Features include animated gauges, swipe navigation, adjustable brightness, and a glowing “TACO TIME” arrival animation. Built with Arduino C++ and PlatformIO in Visual Studio Code.

The six pages include:
1. Boost/vacuum: 15 PSI boost scale, glowing needle, blue-to-red numbers, peak boost, intake temperature, coolant temperature, and voltage. Numbers can display readings above the dial’s maximum.
2. Oil pressure: Ford-specific pressure readings when supported by the vehicle.
3. Coolant temperature: Dedicated temperature gauge.
4. GPS speed/trip: MPH, distance, moving time, satellite status, and End/Save/Reset controls.
5. Engine RPM: Live tachometer.
6. Taco Bell locator: Nearest saved restaurant, direction arrow, distance, and nearby list. Red at 3 miles, orange at 1.5 miles, green within ¼ mile, and a pulsing green light trail at 750 feet or closer.
The current restaurant database contains 186 Michigan locations around Westland, excluding Ohio and Canada. Directions show straight-line bearing and distance; they are not turn-by-turn navigation.
The hardware breakdown:
Component	Purpose
Waveshare ESP32-S3-Touch-AMOLED-1.75-G	Main board with dual-core ESP32-S3, 466×466 AMOLED touchscreen, 16 MB flash, and 8 MB PSRAM. Choose the -G GPS version.
LC76G GPS receiver	Already onboard the -G board; supplies position, speed, and travel direction.
GNSS ceramic antenna	Included with the GPS version; connects to the board for satellite reception.
KONNWEI KW901 Bluetooth LE OBD-II adapter	Plugs into the truck’s OBD port and sends diagnostic readings wirelessly. Use the BLE version tested with this project.
USB-C data cable	Firmware uploading and power.
Regulated 5 V USB power source	Vehicle USB outlet or automotive USB adapter to power the display.
Enclosure/gauge mount — optional	Protects and secures the board in the cab.


Software needed: VS Code, PlatformIO, and the supplied project with its bundled libraries. Normal operation requires no phone, Wi-Fi, or internet connection. Other vehicles and adapters may need configuration changes.
