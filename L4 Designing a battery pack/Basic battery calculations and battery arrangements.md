Now that we have calculated the average energy needed for propulsion of the vehicle with respect to a WLTC Drive cycle, we can take that data and move on to selecting a battery to accommodate the energy consumption.

The battery parameters have a significant influence on other components and attributes of the vehicle, like:

- Maximum traction motor torque
- Maximum regeneration brake torque
- Vehicle range
- Vehicle total weight
- Vehicle price

>Pretty much all major aspects of a pure electric vehicle depend on the parameters of the battery.

Before we move on to selecting our battery, we need to calculate all the secondary appliances in a vehicle that will require power as well.

On top of the energy needed for propulsion **i.e, E~p~= 31.7 Wh/km calculated in the previous lesson,** the battery must supply the energy for the vehicle’s auxiliary devices E~aux~ [Wh/km], like 12 V electrical system. Also, we have to consider the efficiency of the powertrain η~p~[-] during the conversion from electrical energy to mechanical energy.

![CodeCogsEqn (19).png](https://demo.pflms.com/markdown_attachments/1809/ZFN6zbtzgahEYD9rYWPOxw)*(1)*

The prolonged electrical loads (headlights, multimedia, etc.) and intermittent loads (brake lights, horns, etc.) use on average **40 W** of electrical power. 

The duration of the WLTC cycle is 1800 s (0.5 h), which gives energy of 20 Wh for the auxiliary loads. 

If we divide it on the length of the WLTC driving cycle (23.266 km), we get an average energy consumption for the auxiliary loads E~aux~ of 0.86 Wh/km.

Even if Wh/km is not really energy but factorized energy, since it’s divided per unit of distance (km), for simplicity, we are going to refer to it as average energy.

The direct current (DC) supplied by the battery is converted into alternated current (AC) by the inverter. This conversion takes place with an associated loss. Also, the electric motor and driveline have some losses which we need to consider. For this exercise, we are going to use an average efficiency η~p~ of 0.9 from the battery to the wheel.

**Replacing the values with **E~p~= 31.7 and E~aux~ = 0.8** in (1) gives the average energy consumption**


![average energy consumed.png](https://www.pupilfirst.school/markdown_attachments/3235/CbnWYI_kw4amc5axkKK_1A)

_We can consider the **Average energy consumption** of our vehicle as the **Total energy consumption** in order to calculate the minimum requirements for the battery_

The battery pack will be designed for average energy consumption of **35.75 Wh/km.**

We have already learned the basics of the working of Li-ion Batteries in the [previous lesson](https://www.pupilfirst.school/targets/10107).

Let's look at **how batteries can be arranged to give us the needed outputs.**

Individual li-ion battery cells may be grouped in parallel and/or series as modules. Further, battery modules can be connected in parallel and/or series to create a battery pack. Depending on the battery parameters, there may be several levels of modularity.

**The total battery pack voltage is determined by the number of cells in series. For example, the total (string) voltage of 6 cells connected in series will be the sum of their individual voltage.**

<img class="mx-auto w-auto md:w-auto" alt="Battery cells connected in series" src="https://do7js0tdxrds1.cloudfront.net/souftkxz3um0d0eo92tvtt7ghsoa?response-content-disposition=inline%3B+filename%3D%22Batt+1.png%22%3B&response-content-type=image%2Fpng&Expires=1693568696&Signature=sI7im7HSBu0iOMoat3wDT10ownuZ0lg-iFoxJ-1JvejxD0aNixr2~WgOSFwE2yfEFjThKmLITTRI8BKNpqah9P2L9j6qaH-Hv4G5axhmrD~1IIKNQnsZ~6edEHx4XxVSJT~68DxKkYaHcT2IBefjJRsg5vLEwaTP3ePKbew9SmC8na5B61-Dspc52n23fUPpyUh5yzTm64a2KVfsh~mHbaS-moAZLdi9Aa70PkgSMBgbesU5I2bsYrIKbOYAY4vk7HOlJypxleCkdCEm1v64y-Gf57jA9W3b6CevLCEgmw33C5KMhfGW0awr14nvxbfcMHDG~7mV1wx5uaGjN5pEVw__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

-=- Source: [BatteryCellsInSeries](https://commons.wikimedia.org/wiki/File:BatteryCellsInSeries.PNG) | License: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)

In order to increase the current capability and the battery capacity, more cells have to be connected in parallel. For example, 3 cells connected in parallel will triple the capacity and current capability of the battery pack.

<img class="mx-auto w-auto md:w-auto" alt="batt 22.png" src="https://do7js0tdxrds1.cloudfront.net/8qmud43op9zneixrsqsjds3tok3r?response-content-disposition=inline%3B+filename%3D%22batt+22.png%22%3B&response-content-type=image%2Fpng&Expires=1693568813&Signature=hgD-tqvQhEtIo5mRBUieT9CjNUn9InmJw1BCYsfD4CAWO7FqW0InY5C202bkikzDl983QTDv-IabLtoFC~FkaNkJ6q8XMKaaMbG5QwWGAMBN~DA-9DLze3I~50eFEzd7pn8q9-98pF7OQHPIGAZKedjJRlJ5YDXAyGz4ZY2z59daQ0nBOvPISEFqet84bGOH9dz98vQG0XiaukyGAd0rVT78V3cRdIwFxUcGOeSn5L4CzwLXukvQpAnET5qmZNRJ8~4~yTpq5l2tbAJAfB3JWzekZxqUFBKBtTxt1LgD51362GuMAFqT4ALrxnzraC6FtaelEBBzZYF3Pln-FtUctA__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

-=- Battery cells in parallel
-=- Source: [BatteryCellsInParallel](https://commons.wikimedia.org/wiki/File:BatteryCellsInParallel.PNG) | License: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)

## Example

The battery pack of an average electric car consists of 10 modules made up of 120 cells connected in series and parallel. Each module contains 4 prismatic cells. The voltage of each cell is 3.7 V and the total voltage of the battery pack comes around 440 V arranged as shown in the image below.

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/kurrcqnua9nn8i7miyp95ai3e3tl?response-content-disposition=inline%3B+filename%3D%22Batt+3.png%22%3B&response-content-type=image%2Fpng&Expires=1693568813&Signature=bJzk1nyvpK7RSgtUczl-okfW0lxnQ7ODA3HBzTkoBF59n1Am7zJ9jqzjrBUEp9C1~kOo0jDy5vJJbt6VSSQKoVa33rioGAhONozE4vjfN5XT2~jTiZRXHhRliKSousuIzGvUQlzbO4GtV-nVxcS5S2kO1mJsZPzglhvaWA3JJVqPs81Ae-IEOOBGy23LZqpGB2KecECiX4Z3n21m-4Jik7~j8n0D0D~dO0nWzUPvaUMilyGdF3jtLpb8iSTmQIpiXE3TnoLBRa06jjwhUnz-sfAdmQxxLHWPuib6GrysaQFuIZuMschYZJmq2SiKocQv~5WvKZ-C-oUmIaOlQz5AcA__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

-=- Source: [JRC technical Report](https://www.google.com/url?sa=i&url=https%3A%2F%2Fpublications.jrc.ec.europa.eu%2Frepository%2Fbitstream%2FJRC123925%2Fbatteries_potential_criteria_final_external_corrected_published_1.pdf&psig=AOvVaw1b5eItRRmUUUT5W93okBja&ust=1627066341967000&source=images&cd=vfe&ved=0CA0Q3YkBahcKEwjw2IHPrPfxAhUAAAAAHQAAAAAQKw) | License: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)