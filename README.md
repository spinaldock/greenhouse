This code monitors the humidity and temperature inside the greenhouse by means of a DHT22 digital sensor, and an operating range is established, with which the internal temperature is controlled. 
If the temperature is higher than the indicated range, it activates 2 relays that activate the extractor and the wet wall pump, cooling the interior until reaching the lower range.
For irrigation, within the NODE-RED UI, there is a calendar option, where irrigation can be scheduled, either by time range, or by a single hour, and irrigation stops automatically
when a certain amount of liters is reached. For this, a YF-S201 sensor was implemented, which counts the number of pulses in a time range. The faster the water passes, the more pulses 
per minute it will have. By empirical measurement, it was determined that 2.25 milliliters per pulse was the most accurate for the calculations. Irrigation is controlled by means of a
solenoid valve, which is activated when the microcontroller sends the signal to the relay.

To facilitate connections, the ESP32-30P-SSR-4CH board is recommended, which has 4 solid-state relays.
