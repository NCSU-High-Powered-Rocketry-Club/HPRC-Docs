# What is FIRM?

FIRM (Filtered Inertial Rotation Module) is HPRC's custom [flight controller](flight_controllers_and_computers.md), with the main purpose of providing real-time [flight data](firm_data.md) to the Airbrakes system and the payload. The idea for FIRM began at the end of the 2024-2025 academic year, and development began during the summer.

# Why FIRM?

FIRM solves a handful of issues that the club has experienced for a while, as well as providing unique benefits:

### 1. Cost
A large reason is cost and replacability. The data collection sensor that the Airbrakes system used prior to FIRM cost $1400, and due to the chaotic nature of rockets, there is always a chance of a failure during launch that could break it. FIRM currently costs around $75 per board to produce, so we typically order 5 boards at once so we don't lose sleep over potentially damaging/frying a board.

### 2. Ease of Use
Every year the payload in the rocket uses some form of sensing technology. You need to know when the rocket has launched, you might need to know when apogee is reached, or maybe the payload must achieve some task once it lands. Before FIRM, a non-negligible amount of time was spent researching how to accomplish these tasks, figuring out how to interface with sensors, and troubleshooting (or frying) these delicate electronics. FIRM strives to be an all-in-one solution to these reoccuring headaches, allowing the payload and Airbrakes team to focus on what actually matters.

### 3. Performance and Accuracy
The actual hardware of FIRM was designed with high-quality sensors taking first priority. Because Airbrakes was a large target use-case, accurate sensors were chosen to compete with Airbrakes' aforementioned $1400 sensor. Surprisingly though, the precision of the data that FIRM provides is largely dependent on the software choices made. Because we know that FIRM will be used in rockets (and rockets have very predictable kinematics), we are able to use advanced data-filtering software to increase the precision of the data by providing a prediction of where the rocket (and FIRM) will go next.

### 4. Size
A slightly less important factor is the physical size of FIRM. Rockets have limitations on space and weight, so designing custom hardware allows us to optimize space heavily. The small form-factor combined with ease-of-use and the low-risk cost makes FIRM accessible even for club members getting their certifications on their personal rockets!

### 5. Club Growth
Last but certainly not least, FIRM has expanded our club immensely, allowing students with electronics and computer science experience to engage in the club much more than before. FIRM also is a continuously improving project with many future features being actively developped and planned.
