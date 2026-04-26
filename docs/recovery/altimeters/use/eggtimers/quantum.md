# Quantum

As one of the lowest priced COTS data-recording Altimeters for hobby rocketry, the **[Eggtimer Quantum](https://eggtimerrocketry.com/home/altimeters-av-bay/)** is a WiFi-enabled device that allows remote charge deployment and stage ignition.

<!-- ![An image of the fully assembled Eggtimer Quasar G3.](../../../../../imgs\recovery\altimeters\use\eggtimers\quasar\Quasar-G3-Full.jpg) -->

Like all Eggtimer products, the device comes with the necessary components, and requires post-purchase soldering following the applicable [guide]<!-- (https://eggtimerrocketry.com/eggtimer-quasar-support/)-->.

<!-- ![An image of all of the Eggtimer Quasar G3 parts, dissassembled and unsoldered.](../../../../../imgs\recovery\altimeters\use\eggtimers\quasar\quasar-parts-g3-disassembled.jpg) -->

Unlike most COTS altimeters, the Quasar (and many other Eggtimer altimeters) do not come with terminal blocks for a switch. This is because Eggtimers with WiFi modules have something called a *WiFi switch*, meaning you can disable the altimeter without needing to turn or press a physical switch. Rocketry associations like TRA and NAR do consider this switch sufficient for safety purposes, but some (including Tacho Lycos) prefer an additional physical switch for an additional level of safety. Since there are no terminal blocks for a physical switch, it is necessary to solder your physical switch in series with your battery connector.

<!-- The CAD file for the Quantum can be found [here](https://drive.google.com/file/d/1PR2ZmyRTRtak5FnZXIlF_6ybPMGH0vzY/view?usp=sharing). -->

## Programming

The Eggtimer Quantum must be programmed digitally using the built-in WiFi module. Since WiFi access is needed, all Quantum's are password protected. The WiFi network name will follow the scheme of Quantum_XXXXXX, and the password will be written on a sticker attached to the bag the altimeter is shipped in, so do **not** lose the bag.

Parts needed:
* Eggtimer Quantum
    + The other end of your battery pigtail should have the needed battery connector 
* 2s LiPo (minimum 300 mAh)
* Physical switch (optional)

1. Plug the LiPo into the Quantum battery port. Please make sure the connectors are oriented correctly so that the red and black wires line up with each other. If using a switch, close the circuit (i.e. pulling the pin, putting the screw in, etc.). The Quantum should make one long beep, followed by a series of three short beeps while booting up.
* Some buzzers may be nonfunctional due to part defects or soldering issues. If no beeps can be heard, confirm the polarity is correct and the WiFi chip is not getting hot before continuing.

2. After the Quantum has booted up, open whatever mobile device you are using to connect to the Quantum. The Quantum should appear in the Other Networks section (or My Networks if you’ve connected to the Quantum before), followed by an underscore and a string of characters.

<!-- ![An image of the iPhone WiFi menu, with QUASAR_8F6877 circled in red.](../../../../../imgs\recovery\altimeters\use\eggtimers\quasar\QuasarWiFi.jpg) -->

These characters vary for every Quantum. Select the Quantum and connect to its WiFi, using the password provided with your device.

3. After connecting to this WiFi, go to your device’s search browser, and search for the ip 192.168.4.1. This should take you to the site for your Quantum’s settings, and you should see the same code as the WiFi name shown at the top.

<!-- ![An image of the QUASAR_8F6877 menu, with parameters like Flight Status, Drogue & main Altitude/Delay, & GPS Status.](../../../../../imgs\recovery\altimeters\use\eggtimers\quasar\QuasarMenu.jpg) -->

4. You can now change your settings for Drogue and Main by hitting the Change button next to their respective settings. DROGUE Delay is the time after apogee that the drogue channel will be powered, in seconds, and MAIN Altitude is the altitude, in feet, where the main channel will be powered. Hit ``Submit`` to ensure any changes are saved.
* If desired, you can change the name of your WiFi network by going directly to the web address ``192.168.4.1/hsetup``

5. After finishing with the Quantum, disconnect from the Quantum’s WiFi and open the circuit if you are using a physical switch. If you are no longer using the altimeter, unplug the LiPo from the altimeter. If the LiPo is the one you intend to use on the field, please check that the battery is fully charged or plug the battery into the charger.
* If the battery is plugged in, DO NOT leave it unattended. The LiPo should be removed as soon as it is fully charged, do not leave it on the charger.

More details to come.

<!-- Last Updated: 04/25/26 -->
<!-- Last Updated By: Alex Key/Mads Groennegaard -->