# Data from FIRM

What data does FIRM collect, anyway? Why is the data important? What does the data tell us about our rocket? These are all common questions about FIRM, so this page explains what each metric that FIRM outputs means.

## Pressure
Pressure is the foundation of rocketry data and provides one of the most reliable estimates of current altitude. Pressure is measured with a **barometer**; when referring to a dedicated device for altitude calculation, it is often called an **altimeter**. Atmospheric pressure decreases as height above sea level increases, according to the following equation:
$$altitude = 145366.45\left[1-\left(\frac{Pressure}{101325}\right)^{0.190284}\right]$$
- Where $altitude$ is in meters and $Pressure$ is in Pascals.

To properly record pressure, air must be able to reach the barometer during flight. Typically, pressure port holes are drilled into the rocket airframe so that the pressure inside the compartment containing the barometer can equalize with the pressure outside the rocket.


## Acceleration
Acceleration is the change in velocity over time. It tells you how fast you are speeding up, slowing down, or changing direction. Flight computers measure acceleration with an **accelerometer** and typically output the value in g's (acceleration due to gravity, $9.81 m/s^2$). Accelerometers also measure the acceleration due to gravity, so when sitting flat on a table, you would expect an output of $1g$. Accelerometers typically output data in the X, Y, and Z directions.

Acceleration is arguably the most useful and versatile metric because it can tell different stories depending on how you analyze it. Here are a few ways to interpret and use acceleration:
- Integrating acceleration over time gives velocity.
- When stationary and measuring gravity, it can be used to calculate tilt.
- It can measure large forces such as motor thrust or recovery events (parachutes, black powder).
- If sampled fast enough, it can detect and measure vibrations.

In the context of FIRM, acceleration is mostly used to estimate velocity through integration and to detect launch and landing.

## Angular Rate
Rocket rotation is critical for building a full flight profile of roll, pitch, and yaw over time. Unfortunately, there is no sensor that directly provides fully defined orientation, but a **gyroscope** provides angular rate. This measures how fast the device is rotating in the X, Y, and Z directions. By integrating this measurement, summing angular rates over time, we can estimate the device's orientation.

There are two issues with angular rate:
- A gyroscope does not provide any information about your initial starting point, so when integrating angular rate, you are starting from an unknown, arbitrary orientation.
- Any small constant error in gyroscope output accumulates during integration and causes orientation to change slowly over long periods, even when stationary. This is known as "gyro drift."

## Magnetic Field
Earth's magnetic field is a useful tool for determining what direction you are facing. Just as a compass points north, a **magnetometer** acts as a three-dimensional compass, providing an (X, Y, Z) vector toward magnetic north. The magnetic field is constantly changing, though, and this vector differs depending on your location on Earth. Without a known location or GPS, the magnetic field vector is usually used as a reference orientation rather than a specific cardinal direction.

Despite these limitations, magnetic field data is still invaluable for correcting the two major flaws of the gyroscope. First, magnetic field provides a stable reference vector that can be used to estimate and correct gyro drift. It can also provide an initial starting point for integration, with one caveat: a magnetic field vector by itself does not provide a full orientation (because a vector direction does not define roll around that direction). However, when combined with an acceleration vector (providing the "down" direction), a fully defined orientation can be estimated and used as a starting point for integration.