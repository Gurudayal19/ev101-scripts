**Adding battery plots to a PDF as suggested in the video is purely optional and just for convenience and for ease of viewing.**

# Searching, comparing and selecting

Now that we know how a battery pack works, we now have to learn the steps that go into building a battery pack. 

First is searching for cell manufacturers available in the market and the products they provide. 

Once that is done, we will move on to gathering all the data of these cells from their datasheets on the internet.

Once you have gathered the required data to fill all the data in the Excel sheet given below.

>For now, the Excel table below is already prefilled for you as an example. But for your simulation, **you will have to go through battery datasheets and find and fill out the properties yourself. You cannot use the example for your submission.**

Download the battery selection files by clicking below and extract them to a separate folder on your computer.


An example of the table and all the parameters that need to be entered by you.

| Manufacturer   |   |   |   |   |   |   |
|----------------|:-:|:-:|:-:|:-:|:-:|:-:|
| Type           |   |   |   |   |   |   |
| Model          |   |   |   |   |   |   |
| Source         |   |   |   |   |   |   |
| Length [m]     |   |   |   |   |   |   |
| Diameter [m]   |   |   |   |   |   |   |
| Height [m]     |   |   |   |   |   |   |
| Width [m]      |   |   |   |   |   |   |
| Thickness [m]  |   |   |   |   |   |   |
| Mass [kg]      |   |   |   |   |   |   |
| Capacity [Ah]  |   |   |   |   |   |   |
| Voltage [V]    |   |   |   |   |   |   |
| C-rate (cont.) |   |   |   |   |   |   |
| C-rate (peak)  |   |   |   |   |   |   |


# Submission
 
## Objective
Build a battery pack by arranging them in series or in parallel to get the Required Watt-hours to travel a **distance of 150 Kilometers**.

The required Watt-hours can be calculated by multiplying the Range by the energy consumed per kilometer.

As an example, the total energy consumption according to our calculation was around **35.75 Wh/km****

Now, let's calculate the needed battery capacity, i.e. 35.75 x 150 = 5362 Watt-hours, or a 5.3-kilowatt-hour battery pack

>**The required watt-hours per kilometres as calculated is gathered from your energy consumption block diagram that you simulated in the previous task

>The Vehicle you are designing is a low power electric scooter, and electric scooters have limited space, thus select a battery with great power to Pack volume[M3] ratio, good power to weight ratio, capacity to price ratio, etc. 

## Rubric:

1. Use the list of 5 Given batteries, select a battery type.
2. Gather battery details from their datasheets and enter them into the Excel table.
3. Simulate the Scilab file and get all the plots that automatically compares various batteries. 
4. Compare all the data from the created plots.
5. Select the best battery type out of the predefined 5 batteries for each question asked in the final quiz.
6. **Assume a Fixed Total Battery output voltage of 60 volts,** i.e. build a battery pack by arranging cells in series or parallel to give out an output of 60 volts.
7. Design a battery to go 150 km on a single charge (i.e. Range: 150 km)
8. Once you have designed the battery pack, enter all the details of your battery with the total energy consumption that you have calculated in the previous level in the questionnaire given below.


### Basically:
As you will be given a list of 5 different batteries from different manufacturers. All you need to do is, find the datasheets of these individual batteries and enter them into the Excel sheet and simulate accordingly. Compare all the plots and specifications and complete the quiz.


### Here are the model Names of the 5 batteries that you need to choose from:

1. Power-sonic Phr-121000 [datasheet](https://www.power-sonic.com/wp-content/uploads/2018/12/PHR-12100%20technical%20specifications.pdf) Price : 5,191/-
2. Samsung INR18650-15Q [datasheet](http://www.batteryspace.com/prod-specs/6615.pdf) Price: 190/-
3. Sony US18650VT C3 [datasheet](https://www.megacellmonitor.com/pdf/vendor_specs/SPEC_SONY_US18650VT.pdf) Price : 500/-
4. LG Chem 18650 HE2  [datasheet](https://cdn.shopify.com/s/files/1/0674/3651/files/LG_18650HE2.pdf?827) Price : 300/-
5. CATL Type 60AH [datasheet](https://www.genuinepower.co.in/lithium-ferrous-phosphate-battery.html) Price : 3000/-

As explained above, use the datasheets from the batteries given above and fill the excel sheet from the downloaded zip file and run the simulation as given in the video. After doing that, get the plots, compare and select the best battery for the scooter we are building. 

>We have given you links to the datasheets to keep answers from all students uniform in this chapter. But you will have to search for your own batteries and datasheets in the final milestone as instructed in the above video.


This is the ideal order that you will be going in while executing the simulation.
1. Fill cell Data.
2. Execute Script
3. Visualise data. 
![1 (1).png](https://www.pupilfirst.school/markdown_attachments/3632/P7-Tt-cjMPyvmUE8mHORMQ)



> This exercise is just to make you proficient in reading datasheets and making you aware of different battery types and architectures. For your convenience, data for 1 battery is already filled, you need to fill the other 4.



## Additional Tips

### Formula for Watt-hour or WH 


![CodeCogsEqn (21).png](https://demo.pflms.com/markdown_attachments/1815/pJdTHRumrc5oDTACYLfiwA)


For example, if you have a 2 Ah battery rated at 5 V, the power is 2Ah * 5V = 10Wh.

**Here are some different shapes of Li-ion Cells**

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/45l8o8nzfe57uv8aqbfhss5wdvsl?response-content-disposition=inline%3B+filename%3D%22Different+types+of.png%22%3B&response-content-type=image%2Fpng&Expires=1693568976&Signature=XbWCLcZNDB3YMzlOedq1MIAJbhx9jTUluwEFP7o8-ISLinEf5rv62clPXDbxz9~opLsZYVuooHhP6l5~3TRbQvk2cT6jPruyqhFcsbSdr65B4ByjbVrnvJFKBPOXqVDXqMnRhHTL9RnYrixO5w3WhFmeZH1Xl29kLBvVzZgL8H1rvCa0PTtqlkmjmW0KFvbn-hjX0dTpt8h38l1b09L7kCIjrIjQqCL6Z6aINTbnMcW1AMQ5Sg2KjmpThnMLhm~fLe4QMCHnA-Z3D7n0K1luXs3IfqDMbAFg6cYNCFT0ZzzBW31UFW4aWQQP4hIKNC7tZ0xOunNkGmLIG3pCK8Zrdg__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">