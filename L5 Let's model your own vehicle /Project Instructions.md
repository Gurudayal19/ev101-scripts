In this lesson, we will list down the approach you need to follow to do this. 

## 1. Select your 2 wheeler.

As a first step, use the list of vehicles along with their spec sheet below to select a vehicle of your choice.

> Important: Please select vehicle only from the list below in your project. 

### **Two wheelers - Scooter**

[Scooty pep plus](https://www.tvsmotor.com/tvs-scootypep/-/media/Brand-Pages/ScootyPep/scooty-pep-plus-bsvi-brochure.pdf)
 
[Yamaha Ray-ZR 125](https://www.yamaha-motor-india.com/theme/v3/pdfs/brochure/ray-zr-streetrally125fihybrid.pdf) 

[Suzuki Access 125](https://static.autox.com/uploads/bikes/brochure/2023/04/suzuki-access-125-brochure.pdf) 

[Hero Pleasure Plus](https://static.autox.com/uploads/bikes/brochure/2021/06/hero-pleasure-plus-brochure.pdf)
 
[Honda Dio](https://static.autox.com/uploads/bikes/brochure/2017/05/2017-Honda-Dio-brochure.pdf)
 
[TVS Jupiter](https://www.tvsmotor.com/tvs-jupiter/-/media/Brand-Pages/Jupiter/brochure/Oct2021/TVS-Jupiter-BSVI-Brochure-13102021.pdf) 

[TVS NTORQ 125](https://www.tvsmotor.com/tvs-ntorq/-/media/Brand-Pages/NTorq/brochure/TVS_NtorQ_XT-Leaflet_8pg_Brochure_24052022_web.pdf) 

[Suzuki Burgman](https://www.bikedekho.com/suzuki/burgman-street/specifications) 

[Hero Maestro Edge 125](https://www.heromotocorp.com/content/dam/hero-aem-website/in/documents/product-brochures/new-maestro-edge-125.pdf)

[Yamaha Aerox 155](https://www.yamaha-motor-india.com/theme/v3/pdfs/brochure/aerox.pdf)

### **Two wheelers - Bike**

[Hero Splendor plus xtec](https://www.heromotocorp.com/content/dam/hero-aem-website/in/documents/product-brochures/splendor-plus-xtec-Brochure.pdf) 

[Yamaha FZS F1](https://static.autox.com/uploads/bikes/brochure/2021/06/yamaha-fz-s-fi-brochure.pdf)

[Yamaha MT-15 Ver 2.0](https://www.yamaha-motor-india.com/theme/v3/pdfs/brochure/mt15v2.pdf)

[Yamaha R15S](https://www.yamaha-motor-india.com/theme/v3/pdfs/brochure/r15s.pdf) 

[TVS Apache RTR 160 4V](https://www.tvsapache.com/assets/pdf/Apache-RTR-160-4V-BSVI-Brochure.pdf) 

[Bajaj Pulsar 150](https://www.bajajauto.com/pdf/Owner's-Manual-Pulsar-150-Single-Disc-Twin-Disc-BS-VI.pdf)

[Yamaha FZS 25](https://www.yamaha-motor-india.com/theme/v3/pdfs/brochure/fzs25bs6.pdf)

[Kawasaki Ninja 300](https://kawasaki-india.com/wp-content/uploads/2021/03/Kawasaki-Ninja-300_brochure.pdf)

[Royal Enfield Bullet 350](https://static.autox.com/uploads/bikes/brochure/2021/03/royal-enfield-bullet-350-brochure.pdf)

[Mahindra Mojo 300](https://mahindramojo.com/assets/images/Brochure%20-%20MOJO%20300%20ABS%20BSVI.pdf)

[BMW S 1000 RR.](https://www.bmw-motorrad.ca/content/dam/bmwmotorradnsc/marketCA/bmw-motorrad_ca/ca_en/modelbrochures/2020_brochures/2020_S1000RR_CAE.pdf)

[Ducati Monster 821](https://imgcdn.zigwheels.ph/brochures/71/890/ducati-monster-821.pdf)

## 2. Select the target specification for your vehicle

Select the target specification for your vehicle. Refer to lesson [Selecting the Target Specifications for the bike](https://www.pupilfirst.school/targets/10109) to recap on how to proceed with this if you have doubts. 

## 3. Finalize specifications, so your vehicle can compete with its ICE Counterpart

Finalize what specifications you want to move the vehicle to compete with its ICE Counterpart. Your electric conversion needs to be able to beat the petrol version of the bike you plan to convert. You can refer to lesson [Finalizing Target Specifications and calculating Traction Force](https://www.pupilfirst.school/targets/10110) where we looked at the first steps to be taken when you want to convert an existing petrol vehicle, and the vehicle was already selected by us. 

- You can assume the coefficient of drag to around 0.5 - 0.6, for your motorcycle/scooter.
 or, you can refer to this [link](http://www.bgsoflex.com/airdragchart.html) for Air drag coefficient and frontal area calculation if you plan on using a different sized vehicle.

- To calculate the frontal area, the rule of thumb is to take the front view image of the car or bike, and draw small boxes on the front view. Then calculate the area of those boxes and that is the frontal area. You can use the size of the tire as a reference, as tire sizes are standard for all vehicles and are easily available. 

> Note: Make sure to collect all the data that is needed to fill in the table, as they are necessary to get all the calculations correct.

## 4. Simulate energy consumption

Simulate energy consumption with the already available Vehicle specs (for example, weight, tires, etc). This was discussed in lesson [Calculating Energy Consumption {Software simulation in Scilab and Xcos - Part 2.](https://www.pupilfirst.school/targets/10112)
> Note: You won't be able to calculate the weight of the vehicle after you convert it to electric as this is an online course and everything you do is simulated. Hence, it's best to consider already available specifications like the weight, tire size, tire friction coefficient, etc. of the vehicle that you are converting.)


## 5. Build the block diagram and calculate the average energy consumption

Next build Xcos block diagram. Refer to the [Scilab Xcos tutorial](https://demo.pflms.com/markdown_attachments/1799/hZD5Ts_9vW009i5TZQ7zxg) if you are stuck anywhere with Xcos. 

You can use the same Xcos block diagram built in the lesson [Calculating Energy Consumption {Software simulation in Scilab and Xcos - Part 2](https://www.pupilfirst.school/targets/10112) that we used to design the 2-wheeler and change the parameters in "scinotes". There is no need to build another block diagram or make any changes, the same diagram can be used for any vehicle. 

Now that you have finished building a mathematical model for your very own electric vehicle and have received your energy consumption figure, it's time to move on to finalizing everything else in your vehicle. This is important because you will be using this same method in the future when you are going to build your own electric vehicle or design an electric vehicle.


## 6. Design a battery pack to manage the calculated energy needs

Design a battery pack to manage the energy needs you calculated in the previous step. You should select at least 5 batteries from the list given below for comparison. 

> Important: Please select batteries only from the list below in your project. 

- Use the battery selection Excel sheet and Scilab script to come up with appropriate comparisons.

- Refer to [basic battery calculations and battery arrangements](https://www.pupilfirst.school/targets/10113) lesson to get all the battery calculations done.

### **LFP**

Prismatic LFP - Manufacturer: Orange, Model: [IFpP40130200-100](https://robu.in/wp-content/uploads/2021/03/871886-Orange-100Ah-3.2V-Prismatic-LFP-Battery.pdf), Price: [INR 6199](https://robu.in/product/orange-100ah-lithium-ion-rechargeable-battery-for-electric-vehicles/?gclid=CjwKCAjw2K6lBhBXEiwA5RjtCTxNkInPE-B6FW-MRIqhVZ2XEH-qhpfsrrLJmNpfmhTXppEmH05UJxoCdGgQAvD_BwE)

Cylindrical LFP - Manufacturer: Orange, Model:  [IFR32650](https://robu.in/wp-content/uploads/2021/06/951488.pdf) Price: INR [499](https://robu.in/product/orange-ifr32650-6000mah-lifepo4-battery/?gclid=CjwKCAjw2K6lBhBXEiwA5RjtCVIdu_9gHmT6GkOMoISvE5HbRhKJBpc2NSFTfoFVb0wft3vcPEktUhoCoz4QAvD_BwE)

### **Different dimension Li-ion**

Cylindrical Li-ion - Manufacturer: LG, Model: [INR21700 M50](https://robu.in/wp-content/uploads/2021/11/DATASHEET-LGM50.pdf) Price: INR [999](https://robu.in/product/lg-inr21700-m50lt-5000mah-1c-li-ion-battery/)

Cylindrical Li-ion - Manufacturer: SAMSUNG, Model:   [INR21700-40T](https://robu.in/wp-content/uploads/2022/06/SAMSUNG-INR21700-40T-Datasheet.pdf) Price: INR [999](https://robu.in/product/samsung-inr21700-40t-4000mah-9c-li-ion-battery/)

### **Standard - 18650 Li-ion**

Cylindrical Li-ion - Manufacturer: LG Chem, Model:  [INR18650 MJ1](https://www.nkon.nl/sk/k/Specification%20INR18650MJ1%2022.08.2014.pdf)  Price: INR [320](https://www.indiamart.com/proddetail/lg-mj1-18650-3500mah-lithium-ion-battery-21443061062.html)

Cylindrical Li-ion : Manufacturer: Samsung SDI, Model: [INR18650-25R](https://dalincom.ru/datasheet/SAMSUNG%20INR18650-25R.pdf) Price: INR [375](https://www.indiamart.com/proddetail/samsung-25r-lithium-ion-rechargeable-cell-21224893655.html)

Cylindrical Li-ion: Manufacturer: Samsung SDI, Model: [INR18650-30Q INR18650-30Q](https://datasheetspdf.com/pdf-file/951041/Samsung/INR18650-30Q/1) Price: INR [340](https://www.indiamart.com/proddetail/samsung-inr18650-30q-3-6volt-3000mah-li-ion-battery-2849512694133.html)	

### **Prismatic Cells**

Samsung Prismatic cell, Model: [SDI 94ah](https://pdf.indiamart.com/impdf/23963434155/MY-271021/samsung-94ah-3-7v-li-ion-battery-6000-cycles-20-yrs-life.pdf), Price: INR [5500](https://www.indiamart.com/proddetail/samsung-94ah-3-7v-li-ion-battery-6000-cycles-20-yrs-life-23963434155.html)

CATL prismatic cell, Model: [QH-LFP48174128-86](https://www.genuinepower.co.in/lithium-ferrous-phosphate-battery.html#catl-type-60ah-3-2v-15000-cycles:~:text=Model-,QH%2DLFP48174128%2D86,-Casing%20material%20for), Price: INR [2100](https://www.indiamart.com/proddetail/lithium-phosphate-battery-21638006155.html) 

### **Pouch Cells**

LG pouch cell, Model: [E63B](https://pdf.indiamart.com/impdf/26747347997/MY-137078227/3-7v60ah-pouch-lithium-cell.pdf), Price: INR [2100](https://www.indiamart.com/proddetail/3-7v60ah-pouch-lithium-cell-26747347997.html)

Ganfeng pouch type cells, Model: [78158240-030Ah](https://pdf.indiamart.com/impdf/2849206539091/MY-11072761/3-2-v-30-ah-pouch-cell.pdf), Price: INR [1200](https://www.indiamart.com/proddetail/3-2-v-30-ah-pouch-cell-2849206539091.html)

>Important: Please make sure that you include all the necessary details as required in your report submission. Each requirement as listed in the report submission will be thoroughly evaluated to assign marks for the submissions.

<img class="mx-auto w-auto md:w-auto" alt="Use the image below of the rider to simulate a person sitting on your vehicle" src="https://do7js0tdxrds1.cloudfront.net/n4d1b1g5z7mcn6iuuy2hibhdpkuk?response-content-disposition=inline%3B+filename%3D%22man-dressed-as-motorcyclist-controls-invisible-motorcycle-stretching-arms-forward-png.png%22%3B&response-content-type=image%2Fpng&Expires=1693828114&Signature=skt9jVasRYeuHG7~GBNKqltUN5HJaDm-jT6phh1Z~cYmyzeGMcTiBf-7ob5fGGRwj4Eun7TS0BCqL0wwnzwIaxHvPc-MvcPyx0Je7ujRtnu-EB8dDh7Uq~VEjgAXojXTrS0weN9pwUzhbyx7mguumxkRbDFB52HbNkuXhWF0GI-M0GIThyGuC0XSS6FOs81SBAsAxyyWWkLf18qQKxK7uiO~zsAbmcO9sjTEWt7ZLyJuPpP5s8m1aSfoOk5sAzl4ZlwlnxXSIp8bC3nLo0jKRpc9rQVXkEgp2djV30kYvWYf~NDMPWSz0X8Su79w5IvYVZg1qjBDwv6Oki13q8lkwQ__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

Once Done, the Image and Calculation would look something like this

<img class="mx-auto w-auto md:w-auto" alt="Frontal Area calculation | Credit : Chetan Agroya" src="https://do7js0tdxrds1.cloudfront.net/oi96kbm6ab35t9hty25g842au3bi?response-content-disposition=inline%3B+filename%3D%22Frontal+Area+calculation.png%22%3B&response-content-type=image%2Fpng&Expires=1693828114&Signature=bXiwp24FrFm5a0LYYvMTmmwgbA54yl3eURxRpX-CUTB9UAaF2Fr0i6U9lTe-5ZBxz4mmQcZOQleNVCbv58mDHwlC5HfuRdHMouZIrp0QkDA8kcRGXPRFdylKEhxmW-hO4Z2ZjggyakYV2p9y3pq~N-rSAt2FU6HM7DtE0eQDVZjSDaEQIiPHuMgTfdOWXVrzK4rNO5uTNrlqLAdcnoXICoptTX9E5C1TgKIj9ola0CAo1LL9nhp9W5G-2kHV-ioMCd~z6hFpJpqUU3vaUBMXwGhoIQP9YJd0huwfQIEQOgKIYTMQBTQd4fTFQxEFMrOClRtTmDuV92HmJt-L9AXGCA__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

> Note: Make sure to collect all the data that is needed to fill in the table, as they are necessary to get all the calculations correct.


## 4. Simulate energy consumption

Simulate energy consumption with the already available Vehicle specs (for example, weight, tires, etc). This was discussed in lesson [Calculating Energy Consumption {Software simulation in Scilab and Xcos - Part 2.](https://www.pupilfirst.school/targets/10112)
> Note: You won't be able to calculate the weight of the vehicle after you convert it to electric as this is an online course and everything you do is simulated. Hence, it's best to consider already available specifications like the weight, tire size, tire friction coefficient, etc. of the vehicle that you are converting.)


## 5. Build the block diagram and calculate the average energy consumption

Next build Xcos block diagram. Refer to the [Scilab Xcos tutorial](https://demo.pflms.com/markdown_attachments/1799/hZD5Ts_9vW009i5TZQ7zxg) if you are stuck anywhere with Xcos. 

You can use the same Xcos block diagram built in the lesson [Calculating Energy Consumption {Software simulation in Scilab and Xcos - Part 2](https://www.pupilfirst.school/targets/10112) that we used to design the 2-wheeler and change the parameters in "scinotes". There is no need to build another block diagram or make any changes, the same diagram can be used for any vehicle. 

Now that you have finished building a mathematical model for your very own electric vehicle and have received your energy consumption figure, it's time to move on to finalizing everything else in your vehicle. This is important because you will be using this same method in the future when you are going to build your own electric vehicle or design an electric vehicle.


## 6. Design a battery pack to manage the calculated energy needs

Design a battery pack to manage the energy needs you calculated in the previous step. You should select at least 5 batteries from the list given below for comparison. 

> Important: Please select batteries only from the list below in your project. 

- Use the battery selection Excel sheet and Scilab script to come up with appropriate comparisons.

- Refer to [basic battery calculations and battery arrangements](https://www.pupilfirst.school/targets/10113) lesson to get all the battery calculations done.

### **LFP**

Prismatic LFP - Manufacturer: Orange, Model: [IFpP40130200-100](https://robu.in/wp-content/uploads/2021/03/871886-Orange-100Ah-3.2V-Prismatic-LFP-Battery.pdf), Price: [INR 6199](https://robu.in/product/orange-100ah-lithium-ion-rechargeable-battery-for-electric-vehicles/?gclid=CjwKCAjw2K6lBhBXEiwA5RjtCTxNkInPE-B6FW-MRIqhVZ2XEH-qhpfsrrLJmNpfmhTXppEmH05UJxoCdGgQAvD_BwE)

Cylindrical LFP - Manufacturer: Orange, Model:  [IFR32650](https://robu.in/wp-content/uploads/2021/06/951488.pdf) Price: INR [499](https://robu.in/product/orange-ifr32650-6000mah-lifepo4-battery/?gclid=CjwKCAjw2K6lBhBXEiwA5RjtCVIdu_9gHmT6GkOMoISvE5HbRhKJBpc2NSFTfoFVb0wft3vcPEktUhoCoz4QAvD_BwE)

### **Different dimension Li-ion**

Cylindrical Li-ion - Manufacturer: LG, Model: [INR21700 M50](https://robu.in/wp-content/uploads/2021/11/DATASHEET-LGM50.pdf) Price: INR [999](https://robu.in/product/lg-inr21700-m50lt-5000mah-1c-li-ion-battery/)

Cylindrical Li-ion - Manufacturer: SAMSUNG, Model:   [INR21700-40T](https://robu.in/wp-content/uploads/2022/06/SAMSUNG-INR21700-40T-Datasheet.pdf) Price: INR [999](https://robu.in/product/samsung-inr21700-40t-4000mah-9c-li-ion-battery/)

### **Standard - 18650 Li-ion**

Cylindrical Li-ion - Manufacturer: LG Chem, Model:  [INR18650 MJ1](https://www.nkon.nl/sk/k/Specification%20INR18650MJ1%2022.08.2014.pdf)  Price: INR [320](https://www.indiamart.com/proddetail/lg-mj1-18650-3500mah-lithium-ion-battery-21443061062.html)

Cylindrical Li-ion : Manufacturer: Samsung SDI, Model: [INR18650-25R](https://dalincom.ru/datasheet/SAMSUNG%20INR18650-25R.pdf) Price: INR [375](https://www.indiamart.com/proddetail/samsung-25r-lithium-ion-rechargeable-cell-21224893655.html)

Cylindrical Li-ion: Manufacturer: Samsung SDI, Model: [INR18650-30Q INR18650-30Q](https://datasheetspdf.com/pdf-file/951041/Samsung/INR18650-30Q/1) Price: INR [340](https://www.indiamart.com/proddetail/samsung-inr18650-30q-3-6volt-3000mah-li-ion-battery-2849512694133.html)	

### **Prismatic Cells**

Samsung Prismatic cell, Model: [SDI 94ah](https://pdf.indiamart.com/impdf/23963434155/MY-271021/samsung-94ah-3-7v-li-ion-battery-6000-cycles-20-yrs-life.pdf), Price: INR [5500](https://www.indiamart.com/proddetail/samsung-94ah-3-7v-li-ion-battery-6000-cycles-20-yrs-life-23963434155.html)

CATL prismatic cell, Model: [QH-LFP48174128-86](https://www.genuinepower.co.in/lithium-ferrous-phosphate-battery.html#catl-type-60ah-3-2v-15000-cycles:~:text=Model-,QH%2DLFP48174128%2D86,-Casing%20material%20for), Price: INR [2100](https://www.indiamart.com/proddetail/lithium-phosphate-battery-21638006155.html) 

### **Pouch Cells**

LG pouch cell, Model: [E63B](https://pdf.indiamart.com/impdf/26747347997/MY-137078227/3-7v60ah-pouch-lithium-cell.pdf), Price: INR [2100](https://www.indiamart.com/proddetail/3-7v60ah-pouch-lithium-cell-26747347997.html)

Ganfeng pouch type cells, Model: [78158240-030Ah](https://pdf.indiamart.com/impdf/2849206539091/MY-11072761/3-2-v-30-ah-pouch-cell.pdf), Price: INR [1200](https://www.indiamart.com/proddetail/3-2-v-30-ah-pouch-cell-2849206539091.html)

>Important: Please make sure that you include all the necessary details as required in your report submission. Each requirement as listed in the report submission will be thoroughly evaluated to assign marks for the submissions.

