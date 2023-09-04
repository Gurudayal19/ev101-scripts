### Simulating WLTC Drive cycle to get accurate range figures.

Now that we have set up our environment, it's time to move forward and start our simulation.

But first, we need to understand all the mathematical expressions that go into calculating the energy consumption of a vehicle, as we will be simulating with the help of these equations.

The method to calculate the average energy needed for propulsion of the vehicle is pretty straightforward. 

The steps are as follows:

1. Determine the mathematical expression of the energy consumption
2. Create a Scilab script file (*.sce) for the vehicle parameters (input data)
3. Create the Xcos block diagram (*.zcos)
4. Run the simulation on the WLTC driving cycle
5. Create a post-processing script (*.sce) and analyse the result

> You could follow these steps or you could watch the video later in this lesson, titled **"Video 1 - Simulating energy consumption"** to get a better idea about the steps to build the simulation and getting it running

#### Mathematical expression of the energy consumption
The energy consumption is calculated based on the road loads. The total road load F~tot~ [N] is the sum of the inertial force, road slope force, road load (friction) force, and aerodynamic drag force.

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/zjjrber7c7f2ycuwi974hx8rcg0i?response-content-disposition=inline%3B+filename%3D%22energy+consumption11.png%22%3B&response-content-type=image%2Fpng&Expires=1693401515&Signature=c9nEnNbePBwZBh3JUGH67qXJTg0g3x1GHQXDZqITfO9uPnCsrRnwtcLCnpIxqsDxPuTfD5cnfhvzxqf3PlacGcKEk5Uec-Pwu8VzIzVJZ4fmVuXLdi~2Cf5Y0Po8Aj-7x~vj3-v7chklMJEGLrcVC3rqx7g3hK3PzN5A9J6gO~I3WEjwNTw8TxUsP80oVyHdoJq8i9BJymGiqAGYy5cEyPaxGdQovPROlxbLtN2iVFCH8CxLJ2WaLNDofNlNa1xEGoWLneE5vjZA0SSKFM8kTLtEQ4srwLportoSAZDR-D~dXrH8Qxmqpt1RESBvajAyuyIotpPHWzxNbxzI5zaL9w__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

---
![CodeCogsEqn (2).png](https://demo.pflms.com/markdown_attachments/1783/qPGRIt6H_s_A0xvzYWjgaw)

where:

- F~i~ [N] – inertial force
- F~s~ [N] – road slope force
- F~r~ [N] – road load force
- F~a~ [N] – aerodynamic drag force

---
The **inertial force** is given by the equation:

![CodeCogsEqn (3).png](https://demo.pflms.com/markdown_attachments/1784/QLUoAPPqYJ5R701MPww-Pw)


where:

- m~v~ [kg] – total vehicle mass
- a~v~ [m/s^2^] – vehicle acceleration

---
The **vehicle acceleration** can be calculated as:


![CodeCogsEqn (5).png](https://demo.pflms.com/markdown_attachments/1787/ENQAXtjtiYtnuIlTwxB1vg)

where:

- Δ~v~[m/s] – speed difference
- Δ~t~ [s] – time difference

---
The **road slope** force is given by the equation:


![CodeCogsEqn (6).png](https://demo.pflms.com/markdown_attachments/1786/0AoSPcyRavLTMVNV9g0lgw)

where:

- g [m/s^2^] – gravitational acceleration
- α~s~ [rad] – road slope angle

---
The **road load (friction) force** is given by the equation:


![CodeCogsEqn (7).png](https://demo.pflms.com/markdown_attachments/1788/oQU4RlVfj4SHoza2liss5Q)

where:

- c~rr~ [-] – road rolling resistance coefficient.

>**road rolling resistance coefficient** and **coefficient of friction** are not the same, Rolling resistance is a force opposing motion, while friction force enables motion, in the case of a wheel. Friction opposes the applied torque at the ground, leading to the net forward reaction force on the car.

Please have a look at the PDF below to get an idea on the differences.

[Doc link - Tire friction and rolling resistance coefficients](https://do7js0tdxrds1.cloudfront.net/svb2e25kgeqng7cun6lda1g9j09z?response-content-disposition=inline%3B+filename%3D%22Tire+friction+and+rolling+coefficients.pdf%22%3B&response-content-type=application%2Fpdf&Expires=1693401515&Signature=WnSAXfYHN40coQW4itcJBKGJ08wxLgN44J9AGC5SY9QVn~sQuiFPYWCN8k7mXgVrGImlECDxn~mGCb5yisavpyS3Rjinl5x6JKTKeP619~DsNX23lzE5EWt8rK7c-2Vz8gce~AlocvwAapnvZ7zaOYZzyJpMZ7mONGBpJCNRBr9Z~G21IBBvb-SfpnOIanZfxQbxB58XgGykfTf5LOWcHV5v5~AhLAkT6BtghnGFZpnUrDmxo2HBzZu4-5DCxWLBNN5RZxgAPrezG8C-oVIFLOXXfn9x1ZvA4XAXqIshJMUFlojAPemoiNymVzj8BKt2495HXfm8ZEhaxkrWhKOqVA__&Key-Pair-Id=K2Q3HDJ6ZAQGFF)

Here is a handy tool to calculate the Rolling resistance : [Click here](https://hpwizard.com/tire-friction-coefficient.html)

To understand more about the differences and get a accurate value for your vehicle visit this [link](https://www.engineeringtoolbox.com/rolling-friction-resistance-d_1303.html)

---
The **aerodynamic drag** force is given by the equation:


![CodeCogsEqn (8).png](https://demo.pflms.com/markdown_attachments/1789/oX1GC7jW4iSRIp9p_b26Iw)

where:

- ρ [kg/m^3^] – air density at 20 °C
- c~d~ [-] – air drag coefficient
- A [m^2^] – vehicle frontal area
- v~v~[m/s] – vehicle speed

> The frontal area of the vehicle can be assumed to be around 0.46m^2^ - 0.84 m^2^if you plan to model the aerodynamic drag for an electric scooter or a commuter bike.

>Commuter bikes are not usually aerodynamically tested and thus aero numbers are difficult to find.

>You can also use this guide: https://www.princeton.edu/~maelabs/hpt/mechanics/mecha_55.htm

Make sure to watch the video below to get a better understanding about aerodynamics.

---

The **total power** P~tot~[W] is calculated as the product between the total road forces and the vehicle speed:


![CodeCogsEqn (9).png](https://demo.pflms.com/markdown_attachments/1790/7EqGOoMNc_NgLZjXOIzCZA)

---

By integrating the total power over time (for the whole duration of the cycle), we get the total energy consumption E~tot~ [J]:


![CodeCogsEqn (10).png](https://demo.pflms.com/markdown_attachments/1791/a9T--OB6_DkjT7YVKaW5xQ)

All the equations above will be used in the Xcos block diagram to calculate the average energy needed for propulsion of the vehicle over the drive cycle.

Now that we know what equations need to be simulated, and the drive cycle we are modelling our vehicle for.

### These are the steps that need to be followed
   1. Upload WLTC data by running the script in the previous target
   2. Enter and Execute the Vehicle Parameters script given below
   3. Build a block diagram and run the simulation

 First, let's upload the WLTC data using the same steps from the previous chapter.

Once, step 1 is complete, let's begin by entering the vehicle parameters (input data).

Below is the script that will be implemented in **scinotes**, similar to the previous lesson where we inserted the script to import the excel file.

```
vehMassKerb = 110 ; // [kg]
vehMassDriver = 80; // [kg]
vehMassfm = 1.05; 
vehMass = vehMassKerb * vehMassfm + vehMassDriver; // [kg] 
vehg = 9.81; // [m/s^2^]
vehcd = 0.52; 
vehfa = 0.46; // [m^2^]
vehro = 1.202; // [kg/m^3^]
roadSlope = 0; // [rad]
roadCrr = 0.02; 
```
> Make sure to execute the above script before building the block diagram


![vehicle parameters.jpg](https://www.pupilfirst.school/markdown_attachments/3233/2sdo_eZVA1ZPngAjMprXLQ)

**Once pasted, click on save and execute. via the execute tab above,**

Here, 
- **vehMassKerb** = kerb weight of the vehicle
- **vehMassDriver**  = weight of the driver
- **vehMassfm** = Mass factor
- **vehMass** = total mass of the vehicle
- **vehg** = acceleration due to gravity.
- **vehcd** = Coeff of drag
- **vehfa** = vehicle frontal area
- **vehro** = air density at 20 °C
- **roadSlope** = Angle of inclination of the road in radians
- **roadCrr** = road rolling resistance coefficient

---


## 3. Now To simulate it in XCOS

Xcos provides a modular approach for complex system modelling, using a block diagram editor. Xcos models are compiled and simulated in a single run. 

**Make sure you have Scilab open**

**With Scilab opened, you can launch Xcos in several ways:**

- by clicking the toolbar icon Xcos toolbar icon


![utilities-system-monitor-65x65.png](https://demo.pflms.com/markdown_attachments/1793/pYC6PM6jHzY9psHfcTpEKw)


- Or, from the menu bar, by clicking **Applications -> Xcos**
- by entering at the Scilab console: **xcos**

When Xcos is launched, two windows are opened by default:

1. A palette browser
2. An editing window

![Xcos-Palette-Browser-Libraries-and-Blocks-227x300.jpg](https://demo.pflms.com/markdown_attachments/1794/xceEUJXKY7Ysi0Zp3wagRQ)*Pallete browser*

The Palette browser has two panes. The left pane contains the list of available predefined palettes (libraries). The right pane contains the available blocks for each palette. By clicking another palette in the left pane, a new set of blocks will appear on the right pane.

![Xcos-new-model-file.jpg](https://demo.pflms.com/markdown_attachments/1795/tur-g5QpFbppPgAJRsJWdg)*Xcos editing window*

The editing window is the Xcos workspace for developing new models (diagrams). To add blocks in the diagram, select the block from the palette browser and drag & drop it in the editing window. 

You can also add a block to the diagram by right-clicking the block in the library and `Add to -> “name of the diagram“`.

----

Now that you know how to open the editor. I request you to play around and build the block diagram given below by dragging and dropping all the blocks from the palette.

If you have any problems, make sure to ask in the Community.

> Note: Make sure you Upload or run the `Upload Wltc data` script and the `Vehicle parameters` script before building the xcos block diagram.


<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/zdun7fb8l0b52imbc35f52mb8num?response-content-disposition=inline%3B+filename%3D%22Xcos+Diagram+Manual-11.jpg%22%3B&response-content-type=image%2Fjpeg&Expires=1693401515&Signature=brJQYO5E2MJW~djXsE9QW101vR02WMnzBQsFlRtV2z3-nq9CYMhmhF6xiZlxV2VlC07xxHCmOk9EqSQNFB9LZWqY3BiTuGFNbIYBCob8xDuaaTmFLZ2PGaOVpoN0Zk5G0U1c7G9xOVlTCCI0B~NCf8F~J4SyIgJAQVDHeCXqS6AMXDXlHKlTLSwmdCUUYeDv8l5fguxN2zhyW5FteinNrCm0Feyw1r5X9D~tugkLKct8-nvEjbKOFyPtd1o~8GKldQoEABeTmEhVsOzqPRILCZ1QLBq662gvtrIol0AISo6gr52Hj4cM-PGwlmla8nSaHJCw-6hf6GtMyMxqxVDOlg__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/wate6a3m4ofcrc82hu1vkxktjvzf?response-content-disposition=inline%3B+filename%3D%22Xcos+Diagram+Manual-233.jpg%22%3B&response-content-type=image%2Fjpeg&Expires=1693401515&Signature=hShU37KIDhvrteTWSeLyapLtQFxNHajD53HQvw9NQ3zRtIG6CnHrkl9UOgy8asFA4FnRvuS2GrDmcA9Jh0SiOxe7nfkm92iOERRlLH-XuEKvj92riu2sNlJqS10k-QihSBqjRqay-GjWI4GY0rcEWYkBd8jJ79krO6rX795BPCqF6xvS1PDSdbEE-QUnVTcAlskTaK3Iq~1W5XRKps9T7ZENx-JGjwipr5W34h~gOaiXTwRYGM42ESSPUAu8Bnonpzu~iv~0HZl0qqmgKLSV-QYK~sWEzNmiFIqLGsh-CQwEI3HkstrgTFt0uNTaA259b9YSiNK1XZNAcqvJdfrldA__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/wate6a3m4ofcrc82hu1vkxktjvzf?response-content-disposition=inline%3B+filename%3D%22Xcos+Diagram+Manual-233.jpg%22%3B&response-content-type=image%2Fjpeg&Expires=1693401922&Signature=mDQYT9jwbne2kL4E1zdtFDS3BMizYUIjW7KRL-VDcZgJXNTTvozlj0IhMS7nGqdPpBQME~h2BXo4IeMUeYyeoYTKPetKXf4r~ELMTvlfns7vSFEvfaTymav7gV5NziyORKHhXocVkgfuGgE4qwsRnn5dOphFI0hrx2eE~3yyP5fTttMm8IPaQU0Ig1i~CXsPByFQ708D0VmwJbtPOr2~koVxFp9OYq85HPv~Sirs2RTb9sdL0ud8Z2s00XlaopxWy0GN-Y1Cd50db6QgX~93hMXfe7LqIkThv~2BguXlm~b~aJ9xsDiRPRZuaSyJ-DhTsNbwYTHTdv38fWpfKZXSTQ__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

<img class="mx-auto w-auto md:w-auto" alt="Empty block diagram before simulation" src="https://do7js0tdxrds1.cloudfront.net/y06fdsqlqkumj3holn4r6xzxb428?response-content-disposition=inline%3B+filename%3D%22block+diagram+2.jpg%22%3B&response-content-type=image%2Fjpeg&Expires=1693401922&Signature=j6AEjf6zLivjjl6ZYkocTWSzvxmjjlEamMMtmiwYz~FXpsj6j~GJv9sHb4pQRkPi1pxJvlxuQ273F1DYWlQiQC4FfaJoLEERgjN6qwGx3In6tS6sFolmQGjX36ej29Jmopro5bfXVjVmdDCnc1cokzSkxs24kEpL45s8ZuloigN5mVy~XtVa5G-myUdgjvnAHoa-j-oU2uLi0Sd4KTaWQnCySDrKyYsFbRh0kNa-XPvZ-FjKuiGuCEdfgdJYFU-IIzz3Pi~38LIkCg5Sdp2zqI20tJF~kg6wqvEwyY6K0qEcd51l6jMd3j82fUtzyJoNNNUcWLlVBw3gl6BrQz8u7g__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

<img class="mx-auto w-auto md:w-auto" alt="Block diagram after simulation" src="https://do7js0tdxrds1.cloudfront.net/nr218qsec2o5oqtgvw6swvhnoff3?response-content-disposition=inline%3B+filename%3D%22simulated+block+diagram.jpg%22%3B&response-content-type=image%2Fjpeg&Expires=1693401922&Signature=tTeUD1SLfvWQcFpnxZ7od0AC6vYcsnTDaTTaYG0~w7aqwMPtGYLxeWDcxyAc76SIXswe6woQvBvApEcqptnXjZ~9R8St4~gy5VJWtzqbaT3Mwgprs7yKH151CDkKNCi~CsxaLwAwXWz-bGRZ6ic5tr69t3daCmKx0nyI2KeIqHAMABwQ4qs~aXLSYDI8gxXlV4r45AH3h2yj1hW0XbcUySVPuEeGLDu8CnDc0sUNSLrAawaICqCNsSMBrOK2wOlGcWrGNtDykXRbKSc67eElSjzLzP8HiS857XW6yXAwMfScqbeYpfkqlokUQkAn-wAEPEUGp~HsNDCEXvRkLZMUIA__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

>Here is a PDF tutorial Explaining [how to get yourself familiar with Xcos](https://demo.pflms.com/markdown_attachments/1799/hZD5Ts_9vW009i5TZQ7zxg)

>Another tutorial that might help -
[Xcos for beginners](https://demo.pflms.com/markdown_attachments/1818/RjZWh2rVfeO8_-S-f6KzLg)
  
After you have built the Block diagram you will need to change some settings: 

1. Click on **Simulation** in the top bar and select **setup**,
2. Enter "1800" in the **Final integration time** as the test cycle only runs for 1800 seconds, so we will be integrating from 0 to 1800.

![setup.jpg](https://demo.pflms.com/markdown_attachments/1800/sA0wddyBX3vnVaJaB9TieQ)

* The Xcos block diagram model is run for 1800 s, which is to total duration of the WLTC drive cycle. 

* A Clock block is used to generate a time step of 1 s. This time step is set because the input data (WLTC speed profile) is sampled at 1 s. 

* The Xcos block diagram model is run for 1800 s, which is  the total duration of the WLTC drive cycle. A Clock block is used to generate a time step of 1 s. This time step is set because the input data (WLTC speed profile) is sampled at 1 s. The speed profile is read with a *From workspace* block. 

* We have already uploaded the speed profile in the previous lesson. This was basically uploading the Excel sheet into a structure variable called **WLTC** containing the speed values and time (e.g. WLTC.time and WLTC.values).


Since the sample time is 1 s, which means Δt = 1, the vehicle acceleration will be calculated as the difference between the current speed value and the previous speed value. In the WLTC driving cycle, the road slope is considered 0 rad, therefore will not have any influence on the energy consumption.

Depending on the sign of the total power, we can distinguish between the acceleration and braking (deceleration) phases of the vehicle. The integration of the power, for a Δt = 1, gives the energy. The acceleration and braking energies are calculated separately and then summed up to give the total energy.

#### From the block diagram above

By dividing the last calculated value of the average energy needed for propulsion of the vehicle **(737.95 Wh)** to the total length of the **WLTC drive cycle (23.266 km)**, we get the average energy consumption of the vehicle, **31.7 Wh/km.**

### Data post-processing
Using a Scilab script we can plot the drive cycle simulation result. In this particular case we are going to plot only the acceleration, braking and total energy.
```
plot(WLTC_vehTotEgy_kWh.time, WLTC_vehTotEgy_kWh.values,'k')
plot(WLTC_vehAccEgy_kWh.time, WLTC_vehAccEgy_kWh.values,'r')
plot(WLTC_vehBrkEgy_kWh.time, WLTC_vehBrkEgy_kWh.values,'b')
xgrid()
xlabel('Time [s]','FontSize',2)
ylabel('Energy [kJ]','FontSize',2)
title('Pupilfirst','FontSize',2)
legend('Total','Acceleration','Braking',2)
```

Running the above script will generate the following plot.


![WLTC-energy-consumption.jpg](https://demo.pflms.com/markdown_attachments/1801/0v8LdyHqyXhKud6DdOfQIg)

The same model can be used for any other vehicle, the only change needed being the input parameters update. Also, the simulation can be run for different drive cycles, like FTP or NEDC or for custom cycles which can also include a road gradient.

### Once we complete the simulation, we can get the average energy consumption. Based on this, we will be selecting a battery for our vehicle.


>The average energy needed for propulsion of the vehicle over WLTC drive cycle is **31.7 Wh/km.** *This value will be used to calculate the total energy required to design the high voltage battery.*