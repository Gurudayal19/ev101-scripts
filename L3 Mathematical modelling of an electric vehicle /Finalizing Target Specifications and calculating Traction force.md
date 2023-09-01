# Finalising the host vehicle and target specifications.

In our case, we are going to focus on the conversion of an urban Scooter with an internal combustion engine into a fully electric vehicle. The model of choice will be the **Honda Activa**, with the main parameters defined in the table below:

| Engine                              | Fan Cooled, 4 Stroke, 100cc SI Engine |
|-------------------------------------|-------------------------------------|
| Maximum torque [Nm]                 | 8.79 Nm                               |
| Engine speed @ maximum torque [rpm] | 4500                                |
| Maximum power [HP]                  | 7.6                                 |
|Maximum power [KW]                   | 5.73                                |
| Engine speed @ maximum power [rpm]  | 8000                                |
| Transmission type                   | Automatic, CVT                      |
| tyre symbol                         | 90/90 R 10                         |
| Vehicle mass (kerb) [kg]            | 107                               |
| Aerodynamic drag, C~d~ [-]            | 0.52 (Assumed)                      |
| Frontal area, A [m2]                | 0.46                                |
| Top speed [kph]                     | 80                                 |
| Acceleration time 0-100 kph [s]     | 22 s                             |


Data collected from [www.honda2wheelersindia.com](https://www.honda2wheelersindia.com/activa6g/specifications)

**The objectives for the electric vehicle are to achieve dynamic performance equivalent to or surpassing that of its internal combustion engine counterpart.**

Based on the analysis of the current EV market and the performance parameters of the base vehicle (internal combustion engine, Honda Activa 6g), we are now going to summarise the high-level requirements of our electric vehicle conversion.


## Battery

- **Nominal voltage [V]** : 48,
- **Chemistry** : Lithium-ion,

## Powertrain	

- **Electric motor type** : Permanent magnet/Synchronous (BLDC motor),
- **VehicleRange [km]** : 100,
- **Top speed [kph]** : 90,
- **Time 0-100 kph [s]** : 20,
- **Kerb weight [kg]** : 110,

>The above specs will also act as our final motor specs - all the battery calculation and energy consumption will be based on this.

In order to achieve the required performance similar to the internal combustion engine version, the electric vehicle will be Hub wheel drive, with a drive unit on the rear axle.

## Next step is to calculate - Traction Force

**One key requirement of our battery electric vehicle conversion is to reach 100 kph from standstill in 15 seconds** (in order to compete with the ICE version)

From this requirement, knowing the vehicle weight, we can calculate what is the total traction force and torque. Also, we can check if the wheel (tire) friction can sustain the required traction force.

**The input data in our calculation is:**

| Parameters                                                               | Value      |
|--------------------------------------------------------------------------|------------|
| Vehicle total weight (vehicle kerb weight x mass factor + driver weight**) | 180 kg    |
| Vehicle initial speed                                                    | 0 kph      |
| Vehicle final speed                                                      | 100 kph    |
| Vehicle initial time                                                     | 0 s        |
| Vehicle final time                                                       | 20 s       |
| Tire radius*                                                             | 0.208 m (Dia = 0.416m)    |
| Tire friction coefficient                                                | 1.0        |
| Gravitational acceleration                                               | 9.81 m/s^2^ |

*Visit [tire size calculator](https://www.calculator.net/tire-size-calculator.html?ctw=90&car=90&cws=10&cc=n&cnws=19&ctype=1&x=67&y=32) to get the Tyre Radius. All you need to do is visit the website and enter the Tyre symbol that we found out in the above table.

** Driver weight considered as 80 kg
Vehicle acceleration times from [Bikedheko.com](https://www.bikedekho.com/honda/activa-125/specifications)

>Note: Make sure you calculate in mm and convert it to meters for calculation.

According to Newton’s second law of motion:

![CodeCogsEqn (12).png](https://demo.pflms.com/markdown_attachments/1802/sqQyH7YK-htHXQthJ9uOPg)*(1)*


From (1) we can write the equation of the required traction force on Dry Concrete/Asphalt as:


![CodeCogsEqn (13).png](https://demo.pflms.com/markdown_attachments/1803/I9M8wIyFBHVLE4Hc4mX1sg)*(2)*

where:

- F~t~ [N] – total traction force
- m~v~ [kg] – total vehicle mass
- v~f~ [m/s] – final speed
- v~i~ [m/s]– initial speed
- t~f~ [s] – final time
- t~i~ [s] – initial time


Replacing the input data into equation (2), gives the total traction force required to achieve 0-100 kph in 20 s:



![Total traction force.png](https://www.pupilfirst.school/markdown_attachments/3230/3uf4QnXMU5itfk_v98Ni6w)


The total required traction torque can be calculated as:

![CodeCogsEqn (15).png](https://demo.pflms.com/markdown_attachments/1805/vWDZjoC8fs53o21DaqvKGA)*(3)*

where:

- T~t~[nm] – total traction torque
- r~w~[m] – wheel radius

Replacing the input data into equation (3), gives the total traction torque required to achieve 0-100 kph in 20 s:



![CodeCogsEqn (1).png](https://www.pupilfirst.school/markdown_attachments/4764/07u67PQ1r7qR4rDtv4C4xQ)

In terms of friction, we can calculate the available friction force as:

![CodeCogsEqn (17).png](https://demo.pflms.com/markdown_attachments/1807/IumR6UmX8DCZHjUCZO9r5w)*(4)*

where:

- F~f~ [N] – friction force
- G~v~ [N] – vehicle weight
- g [m/s^2^] – gravitational acceleration
- μ~f~ [-] – friction coefficient (wheel-road)

Replacing the input data into equation (4), gives the available friction force:


![Total friction force.png](https://www.pupilfirst.school/markdown_attachments/3231/VYO4ixV5LYWGvQh_2FAXTA)


Since the available friction force is bigger than the total traction force, assuming that there is no slip between the wheels and road, the total traction force can be applied at the wheels to achieve the 0-100 kph acceleration time.

By these calculations, we can finalize the required torque and go ahead in selecting appropriate motors.

## Introduction to selecting a Motor

We have already gone through the different types of motors and how they work in the previous targets, we will use that knowledge and select a motor to satisfy our torque requirements. 

From the equation above, we have calculated the required torque (T~t~) as **52 nm** to achieve 0-100 kph in 20 seconds. 

Let's now look at motors in the market that have a torque value of 52 nm or higher. It is usually best practice to have a motor with torque ratings slightly higher than calculated in case of emergencies or tricky situations but, while looking for a motor online, you will know that manufacturers sometimes do not provide torque figures in their listings, only the motor power is specified. So to solve this problem, luckily Torque and Power are directly proportional to each other. This means torque increases with an increase in power, and there is a formula for that as well. 

You can use the table shown below as a reference to select an appropriate motor. 
>Please note all the values given below are estimates and you will need to contact motor manufacturers to get accurate numbers. But you can use the table as a starting point. 

If you find the below table hard to understand, you can also refer to the spreadsheet in the link here: [Motor selection spreadsheet](https://docs.google.com/spreadsheets/d/1rpKi7rQiGS8RPP-X75QEdp_YvQCAcB0dRfAml3LS7Lc/edit?usp=sharing)

| Power | Power |  rpm |  rpm |  rpm |  rpm |  rpm |
|:-----:|:-----:|:----:|:----:|:----:|:----:|:----:|
|       |       | 3450 | 2000 | 1750 | 1000 |  500 |
|   hp  |   kW  | (Nm) | (Nm) | (Nm) | (Nm) | (Nm) |
|   1   |  0.75 |  2.1 |  3.6 |  4.1 |  7.1 | 14.2 |
|  1.5  |  1.1  |  3.1 |  5.3 |  6.1 | 10.7 | 21.4 |
|   2   |  1.5  |  4.1 |  7.1 |  8.1 | 14.2 | 28.5 |
|   3   |  2.2  |  6.2 | 10.7 |  12  | 21.4 | 42.7 |
|   5   |  3.7  |  10  |  18  |  20  |  36  |  71  |
|  7.5  |  5.6  |  15  |  27  |  31  |  53  |  107 |
|   10  |  7.5  |  21  |  36  |  41  |  71  |  142 |
|   15  |   11  |  31  |  53  |  61  |  107 |  214 |
|   20  |   15  |  41  |  71  |  81  |  142 |  285 |
|   25  |   19  |  52  |  89  |  102 |  178 |  356 |
|   30  |   22  |  62  |  107 |  122 |  214 |  427 |
|   40  |   30  |  83  |  142 |  163 |  285 |  570 |
|   50  |   37  |  103 |  178 |  204 |  356 |  712 |
|   60  |   45  |  124 |  214 |  244 |  427 |  855 |
|   70  |   52  |  145 |  249 |  285 |  499 |  997 |
|   80  |   60  |  165 |  285 |  326 |  570 | 1140 |
|   90  |   67  |  186 |  321 |  366 |  641 | 1282 |
|  100  |   75  |  207 |  356 |  407 |  712 | 1425 |
|  125  |   93  |  258 |  445 |  509 |  891 | 1781 |
|  150  |  112  |  310 |  534 |  611 | 1069 | 2137 |
|  175  |  131  |  361 |  623 |  712 | 1247 | 2494 |
|  200  |  149  |  413 |  712 |  814 | 1425 | 2850 |
|  225  |  168  |  465 |  801 |  916 | 1603 | 3206 |
|  250  |  187  |  516 |  891 | 1018 | 1781 | 3562 |
|  275  |  205  |  568 |  980 | 1120 | 1959 | 3918 |
|  300  |  224  |  620 | 1069 | 1221 | 2137 | 4275 |
|  350  |  261  |  723 | 1247 | 1425 | 2494 | 4987 |
|  400  |  298  |  826 | 1425 | 1628 | 2850 | 5699 |
|  450  |  336  |  929 | 1603 | 1832 | 3206 | 6412 |
|  550  |  410  | 1136 | 1959 | 2239 | 3918 | 7837 |
|  600  |  448  | 1239 | 2137 | 2443 | 4275 | 8549 |

<img class="mx-auto w-auto md:w-auto" alt="Power (Kw) vs Torque(Nm) @ 1000 RPM" src="https://do7js0tdxrds1.cloudfront.net/zyzekrh4u4grsmaborrn1meshq96?response-content-disposition=inline%3B+filename%3D%22Power+%28Kw%29+vs+Torque%28Nm%29+%40+1000+RPM.png%22%3B&response-content-type=image%2Fpng&Expires=1693401031&Signature=rSXIAE0N0892SKlLQhJWXY1H2Vy856dm88T5EqqEzMo5J~NlOveL5HMtDA6MiriTeSEsKrOxvUj-q-XqB47OxF5Ew8HrOoPzkLqAlaXkVkR7vwjZwtJgpAQ4Tt5FGq8z-sP0UKZ~bOoHOV-hLF75p4ABrMbJnIGhAYlvD-MMJfSEkjs~68mZ9C-~d-c-W3V0u~0wUXHBZPnad~n~d-FDMb0QZuL8jiq8BEzM4kHtyQb3mDp40TRzV8bw2rDKCo4gn075jbbjOTht1Yt-FczVIg4qPIp9Jhvzukmqt5uAWRiLyIlZ3NOKg45wCmt7L9QqHmVqkvFNm6C~8aSAyI-bRA__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

Torque in SI units can be calculated as

**T(Nm) = PW 9.549 / n**

where

* TNm = torque (Nm)
* PW =  power (watts)
* n = revolution per minute (rpm)

>In the next lesson, we are going to focus on the energy consumption of the vehicle over a standard homologation cycle. This will serve as a basis for the design of the battery.
