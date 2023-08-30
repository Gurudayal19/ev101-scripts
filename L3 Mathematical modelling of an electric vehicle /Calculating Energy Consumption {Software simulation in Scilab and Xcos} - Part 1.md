Now that we have calculated the necessary torque required to satisfy our *acceleration* and *top speed* requirements, let's select *battery size*.

The **battery** of an electric vehicle (EV) is one of the most important components since it dictates the dynamic performance, range and charging time of the vehicle. To calculate the size of the battery, we need two main inputs: the **average energy consumption** and the **range of the vehicle**.

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/8mssj2b9ooj5ps5rgso0lraqxmjh?response-content-disposition=inline%3B+filename%3D%22energy+consumption.png%22%3B&response-content-type=image%2Fpng&Expires=1693401411&Signature=iExMPOfv9aZ~UPlVO~f-WOl7dYu6yYiFLJVaESudUDXhATfFsXQO1Y7jZ1TN8DTbWTYzuWfckLmX6m-N~agGiX0a1QdFIynAL~YDOuHb9ay44Np9ncv4QXqJvExQaLoZSzrstnxPJSrnBmwioWZzVGGvux~TmKl5CEfFlq7ri8YFkZHgEfAsZYkwGNYJVmoO4bq3jcqf7ZD0s~rpwYu~5qDXHDhSzRuhg-XIn7QYXMNJeLS03QlQkOPcBkT31XXQ4u06EP--XCKkNcw3ZK6R4dJfcsaKbbV~FtBrlKCDQBfif-qAPkWWGoc-P~a9Q7JnMy2BNhJ-wIVYC9Eg3rGzww__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

# Energy Consumption of a vehicle

There are two ways in which we can calculate the energy consumption of a vehicle
- NEDC Testing
- WLTP Testing

While the NEDC test determines test values based on a theoretical driving profile, the WLTP cycle was developed using real-driving data, gathered from around the world. WLTP, therefore, better represents everyday driving profiles.

## WLTC drive cycle
The average energy consumption of the vehicle *E~avg~ [Wh/km]* will be calculated on a homologation cycle. 

For our example, we are going to use the WLTC drive cycle. The test procedure WLTP (Worldwide harmonized Light vehicles Test Procedure) contains several driving cycles:

- Class 1 – low-power vehicles with PW~r~ <= 22
- Class 2 – vehicles with 22 < PW~r~ <= 34
- Class 3 – high-power vehicles with PW~r~ > 34

Where *PW~r~ [kW/Tonne]* is the power-to-weight ratio, defined as the ratio between the rated engine power and kerb weight.


![CodeCogsEqn.png](https://demo.pflms.com/markdown_attachments/1772/gzY8nxYPS7KIXjkQlVadbw)


Our target is to convert the Honda Activa into a battery electric vehicle (BEV), and therefore we need to understand what is the current energy consumption of the vehicle. 

From the previous task, we can extract the maximum power and kerb weight from the spec table and calculate the power-to-weight ratio:


![power to weight ratio.png](https://www.pupilfirst.school/markdown_attachments/3232/g3RnVeYaWUFMMy4F1pj8-g)
>Since the vehicle’s PW~r~ is bigger than 34, we are going to use the WLTC Class 3 driving cycle to calculate the energy consumption.


![Speed-profile-for-WLTC-Class-3-driving-cycle.png](https://demo.pflms.com/markdown_attachments/1774/PJmsmJWVxpFEor6rbgbxIQ)*Image: Speed profile for WLTC Class 3 driving cycle*


The parameters of the WLTC Class 3 cycle are summarized in the table below:

|                                   | Low   | Medium | High  | Extra High | Total |
|-----------------------------------|-------|--------|-------|------------|-------|
| Duration, s                       | 589   | 433    | 455   | 323        | 1800  |
| Stop duration, s                  | 150   | 49     | 31    | 8          | 235   |
| Distance, m                       | 3095  | 4756   | 7162  | 8254       | 23266 |
| % of stops                        | 26.5% | 11.1%  | 6.8%  | 2.2%       | 13.4% |
| Maximum speed, km/h               | 56.5  | 76.6   | 97.4  | 131.3      |       |
| Average speed without stops, km/h | 25.3  | 44.5   | 60.7  | 94.0       | 53.5  |
| Average speed with stops, km/h    | 18.9  | 39.4   | 56.5  | 91.7       | 46.5  |
| Minimum acceleration, m/s^2^        | -1.5  | -1.5   | -1.5  | -1.44      |       |
| Maximum acceleration, m/s^2^        | 1.611 | 1.611  | 1.666 | 1.055      |       |

The method to calculate the energy consumption is straightforward, and it makes use of the Scilab/Xcos simulation environment. 

----

>Everything explained in the video above is explained below as well, so that it is easier to follow and understand. if you are confused, please watch the video again. 

## 1. Setting up the Simulation Environment

We will now need to install and Setup Scilab, Follow the steps below to install and set it up.

### Step 1. Download Scilab

Click [here](https://www.scilab.org/download/6.1.0) to go to Scilab website, under the *Download* section and choose your installation package. For windows operating systems the are two versions: 32 and 64-bit. Download the one matching your operating system specification.

When the download is complete you’ll have on your disk drive a *.exe file (e.g. Scilab-5.4.0.exe)

### Step 2: Run *.exe file

### Step 3: Select the language to be used during the installation process

### Step 4: Launch the Scilab Setup Wizard

### Step 5: Read the License Agreement

### Step 6: Review all installation settings

### Step 7: Launch Scilab
At the end of the installation, if you check the box for “Launch Scilab”, when you click the “Finish” button, Scilab will be launched.

Click the “Finish” button to exit the Setup Wizard.




![Scilab screen.jpg](https://www.pupilfirst.school/markdown_attachments/6316/wr3zglnbr5FLyIATVoNocQ)


When you launch Scilab you’ll get the start screen as in the image above


## 2. Building an Environment

Create a folder Named **"Electric vehicles"** on the desktop, or where-ever you like.

This will be the folder where all our project files are stored.

**Important note! unless all the required files are stored in the same folder, the simulation wont work.**


## 3. Acquiring the WLTC Test cycle Data

Click on the link below to Download the data, Make sure you store it in  the *Electric vehicles* folder created in the previous step.

[Download WLTP-DHC-12-07e.xls](https://demo.pflms.com/markdown_attachments/1780/BBDYix0qAUzkv4FVzSxZ-w)

## 4. Importing xls (Excel) data into Scilab and Xcos.

There is a predefined Scilab function which can read the content of *.xls files. The Scilab function **xls_read()** reads a sheet from an excel file and saves the data in the Scilab workspace. 

The **xls_read()** function reads an excel sheet given a logical unit on an excel stream and the position of the beginning of the sheet within this stream. It returns the numerical data and the strings contained by the excel cells.

The **read_xls()** function can be used to read all sheets from an excel file in one function with a single function call.

The function can be called as:
```
[Value,TextInd] = xls_read(fd,Sheetpos) 
```
**where:**

- **fd** – a number: the logical unit on the Excel stream returned by xls_open() Scilab function
- **Sheetpos** – a number: the position of the beginning of the sheet in the Excel stream. This position is one of those returned by xls_open()
- **Value** – a matrix of numbers: the numerical data found in the sheet. The cells without numerical data are represented by NaN values
- **TextInd** – a matrix of indices with the same size as Value. The 0 indices indicates that no string exists in the corresponding Excel cell. A positive index i points to the string SST(i) where SST is given by xls_open()

**Don't worry, you don't have to type your own code. It will be given to you in the coming steps. This is just to make you understand what the code does**

>Important note: Only excel file version (2003) are handled.

### Let’s import the data describing the WLTP speed profile. The file can be found here[]:

The data will be first imported into Scilab, stored into a variable, and used later in Xcos for simulation purposes.

**Step 1**. Save the *.xls file after downloading, in the current Scilab working folder, i.e "Electric vehicles"

**Step 2**. Open the *.xls file and examine the data you want to import. 


![xls.jpg](https://demo.pflms.com/markdown_attachments/1781/qbn5dUHX0CuM6eMuLneloA)

In this example, the data is located in the second sheet, named **WLTC_class_3**. We will import the WLTP speed profile, which consists of time values and speed values. 

- **The time values**, in s, begin in the 8th row and 3rd column (C), with value 0. 

- **The speed values**, in kph, begin in the 8th row and 5th column (E), with value 0.0. If you scroll down towards the end of the table, you’ll see that the last data points are in the row 1808.


**Step 3**. Open SciNotes (Applications>Scinotes) and create a script file with the following content:

```
clear()
clc()
//Decode ole file, extract and open Excel stream
[fd,SST,Sheetnames,Sheetpos] = xls_open('WLTP-DHC-12-07e.xls');

//Read second data sheet
[Value,TextInd] = xls_read(fd,Sheetpos(2));

//close the spreadsheet stream
mclose(fd);

//load WLTP time and speed values in structure
WLTC.time = Value(8:1808,3);
WLTC.values = Value(8:1808,5);

//plot WLTP speed profile
plot(WLTC.time,WLTC.values)
xgrid()
xlabel("Time [s]")
ylabel("Vehicle speed [kph]")
title("PupilFirst AICTE-LITE")
```

The file is opened with the Scilab function xls_open(). The data from the second sheet, Sheetpos(2), is read by the xls_read() function and assigned to the Value variable. Further, the WLTP time and speed values are assigned to the WLTP structure.

Notice that from the variable Value we extracted the data between rows 8 and 1808 and columns 3 and 5, as described in Step 2.

Save the Scilab script as *.sce file in the same Scilab folder ("Electric vehicles" folder).


**Step 4**. Run the Scilab script and visualize the data.

After running the script we’ll get the following graphical image:


![Graphic window number 0.png](https://demo.pflms.com/markdown_attachments/1782/svClmkYXq6wTGwhLCBAfVw)

As you can see, the data has been correctly imported, all 1800 time and speed values being plotted.

---
**Now that we have our simulation environment up and running, let's move on to simulating our energy consumption in our vehicle in the next lesson.**

--------
### To understand SciLab and Xcos modelling better, here is a great youtube playlist by IIT Bombay explaining Scilab and it's uses as well as benefits. 

### [IIT Bombay Scilab Tutorial Playlist](https://www.youtube.com/watch?v=1lC6_nDnvLU&list=PL7WFbgpeASD1vxft2QhiTbnXlp6y5CF6J&index=2)