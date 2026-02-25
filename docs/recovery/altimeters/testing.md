# Altimeter Testing

Altimeter testing is done to ensure the sensors are functional before a flight.
The testing setup used by HPRC is placing the altimeter in a vacuum chamber with led lights attached to the pyro outputs. When air is removed from the chamber the internal pressure decreases which simulates an increase in altitude. When air is added back into the chamber, the altimeter should detect the increase in pressure, assume the altitude is decreasing, and fire the "charges" at the approprite times. The leds will light up, one at apogee (right after the vacuum is turned off) and another at main (some time after ). If each led lights up at the correct time the altimeter is deemed okay for flight. This is a rudimentary test that only checks the functionality of the barometric sensor and not the accuracy. 

Other grounds tests include: