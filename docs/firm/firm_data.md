# Data from FIRM

What data does FIRM collect anyways? Why is the data important? What does the data tell us about our rocket? These are all common questions that are asked about FIRM, so this page aims to explain in detail what every metric that FIRM outputs actually means.

## Acceleration
Acceleration is the change in velocity at a given moment of time. It tells you how fast you are speeding up, slowing down, or changing direction. Flight computers measure acceleration with an **accelerometer**, and typically output the value in g's (acceleration due to gravity, $9.81 m/s^2$). Accelerometers also will measure the acceleration due to gravity, so when sitting flat on a table you would expect the output to be $1g$. Accelerometers typically output data in the X, Y, and Z direction.

Acceleration is arguably the most useful and versatile metric that can paint different pictures depending on how you look at it. Here's a few different ways to interpret and use acceleration:
- Integrating (summing up acceleration over time) will get velocity
- When stationary and measuring gravity, it can be used to calculate tilt
- Can measure large forces such as motor thrust or recovery events (parachutes, black powder)
- If sampled fast enough, it can detect and measure vibrations

In the context of FIRM, acceleration is mostly used when integrated for velocity, and to detect launch/landing

## Angular Rate
The rotation of the rocket is critical for getting a full flight profile with the rocket's roll, pitch, and yaw over time. Unfortunately there isn't a sensor that directly gives fully-defined orientation, but a **gyroscope** will give angular rate. This will measure how fast the device is rotating in the X, Y, and Z direction. By integrating this measurement, summing up the angular rates over time, we can calculate the device's orientation!

There is a catch though: A gyroscope does not provide any information about your initial starting point, so when integrating angular rate you are starting from an unknown, arbitrary orientation.

## Magnetic Field
Earth's magnetic field is a useful tool to figure out what direction you are facing. Just like how a compass points North, a **Magnetometer** acts as a three-dimensional compass, providing a vector (X, Y, Z) of Earth's magnetic field. The magnetic field is constantly changing though, and the vector is different depending on your location on Earth as well. Without a known location or GPS, the magnetic field vector is usually only used as a reference orientation rather than a specific cardinal direction.

Despite the limitations, magnetic field is still invaluable for correcting two major flaws of the gyroscope. When integrating angular rate, any small constant error will quickly add up and cause your orientation to change slowly over long periods of time, even when being stationary. This is known as "gyro drift". Magnetometers provide a stable reference vector that can be used to estimate and correct the error in your gyroscope.

The other flaw of the gyroscope is the lack of initial starting point. A magnetic field vector by itself does not provide a full orientation (because a vector direction does not define the roll around that direction), but when combined with an acceleration vector (providing the "down" direction), a fully-defined orientation can be found and integrated upon with angular rate.