# Altimeters
Altimeters typically utilize barometric pressure sensors to calculate the altitude of a rocket during flight and trigger recovery events. Use of altimeters for triggering of recovery events is called electronic deployment.

A deployment capable altimeter commonly features two or more pyro outputs which ignite ematches at desired altitude for recovery. They also typically have a buzzer for indicating the status of the altimeter and will beep out the max altitude following the flight. 

Some altimeters such as the Fluctus and some Eggtimers have wifi and telemetry capabilities.
Altimeters can also feature IMUs (inertial measurement units) for recording acceleration and gyroscopic data during flight.

The wiki features guides for use and programming of commonly used altimeters.

There are non-deployment capable altimeters such as the [Jolly Logic AltimeterOne](https://jollylogic.com/products/altimeterone/) which only measures altitude and cannot trigger recovery events. These are used mostly for low power rockets or rockets with only motor ejection separation.

## Standard Practice for Altimeter Use

Altimeters should always be able to be armed and disarmed from the outside of the rocket. This is done using [switches](#switches).

### Redundancy
A common safety practice when using electronic deployment is to use redundant altimeter. This means using a second "backup" altimeter in addition to the primary one to ensure the rocket is still recovered safely in the event of a failure. To have the best redundancy and safeguard against the most failure modes, secondary altimeters should have completely separate batteries, switches, ematches, and charge wells. It is also wise to use a larger black powder charge to prevent against a separation failure. Additionally, it is recommended to use two different brands of altimeter as further redundancy protect against any potential model specific edge cases. This comprehensive redundancy will allow for the primary altimeter to feature any of the following failure modes and the rocket can still have a safe recovery:

- Sensor failure
- Loss of power or brownout
- Ematch failing to ignite
- Wiring failures
- Failed separation after charge ignition (secondary charge is typically made larger)

The common deployment scheme for altimeters is firing a charge at apogee to deploy a chute, and the backup altimeter firing 1 second later. Then, if it is a dual deployment flight, the altimeter will fire another charge at around 500-800ft agl to deploy the main chute, with the backup firing 50-100ft lower. This main deployment altitude is chosen by the user when programming the altimeter and is based on minimizing velocity at landing. More info about deployment can be found [here](../deployment.md).


### Switches
Power switches are used for basically all electronics in rocketry and are always used with altimeters. It is essential to be able to control the power of the altimeters without disassembling the rocket, meaning an externally accessable switch is necessary. 

Some altimeters such as the StratologgerCF and the EasyMini have a built in switch which allows for direct wiring of the switch to the altimeter, however some do not have this feature. In that case you must wire the switch in series with the power source. When designing a rocket's avionics bay, it is always important to ensure that the altimeters will be capable of remaining powered off during the assembly of the rocket. It is always necessary to keep the altimeters disconnected from power if they are attached to live charges until the rocket is vertical on the launch pad. More info on the safety of altimeters can be found [here]()

The various switches that the club utilizes are listed below.

#### Pull Pin Switch
The coolest one. Pull pins use a microswitch and control the state using a physical pin that slides in and out of the 3D printed enclosure. The cool part is that you can put a remove before flight tag on the pin and it makes the rocket look super official. These are manufactured by [Lab Rat Rocketry](https://www.invertedpursuitslab.com/shop/category/pull-pin-switches-7) but can also be made DIY.

#### Screw Switch
- standard
- fingertech

#### Twist and tape
The tried and true method. This is the simplest switch you can use as it requires no extra hardware. Route the two switch wires to the outside of the rocket through a pressure port. When you are ready to arm, simply twist them together and tape it to the rocket. **NOTE:** make sure you are not covering the pressure port hole, the altimeters still need the outside air.
Always leave the wires taped to the outside of the rocket so you are still able to disarm.

#### Wifi Switches
Wifi switches are found on many Eggtimer altimeters and allow for arming of the device using your phone. This can be convient however it is still always recommended to use a physical switch as well. The altimeter is still receiving power before it is armed with the wifi switch and thus can be considered a hazard. Despite this, Tripoli and NAR consider WiFi switches sufficient disarming and do not require a physical. It is up to your personal disgression, but physical switches are always used by the club.







---

*Created by Aidan M.*
*Last Edited by Aidan M. on 05-01-2026*