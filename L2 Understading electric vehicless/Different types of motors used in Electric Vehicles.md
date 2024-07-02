[Content Suggestions: This content can be broken down into two chapters, and some more content like https://www.youtube.com/watch?v=CWulQ1ZSE3c or
https://youtu.be/bCEiOnuODac?feature=shared can be added in the future]: #

In the world of internal combustion engines, no two are identical due to various configurations and features. One might have expected a single best engine type to emerge, but the diversity caters to individual needs. This trend extends to electric vehicles, but the options are simpler: **DC motors** and **Induction motors**. We'll focus on Brushless DC motors and AC induction motors for electric vehicles.

First, let's understand what an electric motor is. It's an electromechanical device converting electrical energy to mechanical energy, shaping our modern world. The basic idea of an electric motor is simple: you input electricity at one end, and an axle (metal rod) rotates at the other end, providing power to drive a machine. But how exactly does this process occur? Exactly how do you convert electricity into movement?

---

Suppose you take a length of ordinary copper wire, make it into a big loop, and lay it between the poles of a powerful, permanent horseshoe magnet. Now, if you connect the two ends of the wire to a battery, the wire will jump up briefly.

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/vz5tvgt7lt1b9szho4sq3r21xo62?response-content-disposition=inline%3B+filename%3D%22AC+%284%29.png%22%3B&response-content-type=image%2Fpng&Expires=1693399996&Signature=mTnLdHlj4FXoSIU~1jDdl8apmL6rUzR17ufWmM3FBorgSGtVKpFHh1zJpRcpYQ8x1Bf0uSeXnl0cabGRDwdYa0tnoNv~cpdRObkUXcsY8gagSJ0Nj3VDSbUpg~awjtJizy6j4kqq7g7kHfyl-ae7g2q-ZLxWJpnZ-fiFm5h9Da~HZlp8B1536yNBcVHBtXbdZ~8je6ym1j45vmu3iBDnR0Li-2KxUP20X25i0aBvGUWJoda6LtjrtoS~I~dOEK7zwLyg6wlw8RFYJrek9w3~HUPPvx5BpHCNG3103vdBshbblU-ztUvN8PkSWCsR93vBf3Jwjk-XFrD2g382P8rhIg__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

It's amazing when you see this for the first time. It's just like magic! But there's a perfectly scientific explanation. When an electric current starts to flow along a wire, it creates a magnetic field all around it. If you place the wire near a permanent magnet, this temporary magnetic field interacts with the permanent magnet's field. Just as two magnets placed near one another either attract or repel, the temporary magnetism around the wire attracts or repels the permanent magnetism from the magnet, causing the wire to jump.
 
You can figure out the direction in which the wire will jump using a method called **Fleming's Left-Hand Rule**.
 
1. Hold out the thumb, first finger, and second finger of your left hand so all three are at right angles.
2. If you point the second finger in the direction of the current (which flows from the positive to the negative terminal of the battery).
3. Point the first finger in the direction of the Field (which flows from the North to the South pole of the magnet), your thumb's will ten indicate the direction in which the wire moves.

![Left_hand_rule.png](https://www.pupilfirst.school/markdown_attachments/3395/kDMOh0QNRL5zjRnR76KTUw)

-=- Left hand Rule | License: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)

And this is the basic science behind an electric motor. However, to turn this scientific discovery into practical technology for powering electric bikes and cars, we need to explore further.

Don't worry, we will dive deep into all the motor types and their uses in EV 201 after you finish this course.

For now, let's understand the **types of electric motors** available, and take a brief look at how they work and what differentiates them.


![Types of motors.png](https://www.pupilfirst.school/markdown_attachments/3392/Ko2pxv9caXa1u_vFxyyjoQ)


## Let's have a closer look.

So, what are these two technologies? How do they work? What differentiates them? And what do they have in common? Let’s start with DC brushless drives, also known as BLDC motors!

<img class="mx-auto w-auto md:w-auto" alt="Figure 1 : BLDC Motor" src="https://do7js0tdxrds1.cloudfront.net/wylvxee1c18k9i0k59y4p6b7qvra?response-content-disposition=inline%3B+filename%3D%22AC%2B%25285%2529.png%22%3B&response-content-type=image%2Fpng&Expires=1719312664&Signature=SnxDm7AMo5wCgIlaZeyKVLZXlBhgEkarYuCaT3mSqc1yh4W~T6-EdB5km1PKDT8jE5HEE-u8gTuoPmtEToiP1w1A4E37o138ayDSLgbZOhsvuau6JGzkZ3Go1mKIlCqYrkxZt~xSTi~PiB~i59-gnPLSaTOWebDx9GAZzuw1nN9cOYiH1IRwzgpWV9lYnczrYGaENqqsTUOQSNd8S~gFf67AxneW7NYHHU3VkCPE0LNQhX9vtsLSGsEGKLKq~xlDk4d9V6zuVKBEH~KkkK61P2jdzm97wlDcGLFyD9yACFKdNInEq3BsoCTiOFn9ckQ3qlitQjTgPs4JCyJMmUe3BQ__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

In brushless motors, the rotor includes two or more permanent magnets that generate a DC magnetic field (as seen from the rotor's perspective). This magnetic field enters the stator core which made up of thin, stacked laminations. The interaction between the magnetic field and the currents flowing within the windings of the stator produces a magnetic interaction between the rotor and stator.

As the rotor rotates, it is necessary that the magnitude and polarity of the stator currents be continuously varied – and in just the right way - such that the torque remains constant and the conversion of electrical to mechanical energy is done efficiently. The device that provides this current control is called an **inverter or a motor controller**. Without it, brushless motors are useless motors.

## Working of a BLDC motor

Let's make it much simpler and understand it better by taking the below example, imagine a donkey with a carrot hung in front of its face; the donkey will proceed to follow the carrot constantly.

<img class="mx-auto w-auto md:w-auto" alt="Donkey Following a Carrot" src="https://do7js0tdxrds1.cloudfront.net/7b2br4rfknbf9bnk6a0fkpnenovb?response-content-disposition=inline%3B+filename%3D%22GIF.gif%22%3B&response-content-type=image%2Fgif&Expires=1719312664&Signature=UcqNlAUaeFFpwkFWV1XPkXuj6ypNtCmYwG1v-mGXbzy~WGrjIKBa--rsJa2bSP1VjvgL0xpQjjSqjdfW1izVmC0fvwJre7NwOb~EtyM5RjMju8vQQnskgI9ZXfbT7qG7iEdYDYp3~NMAa01NGD1qom~r8JZltcBDA22AijkXx7qTs4dy5uA3TcEwnWQn~jO4XA8FKGIdb3yBO7vRORFkJ0hil6YRTd396ECZW~p7BLTBwUBzY0~O-Jb8toxOc7B24rWETHcX~tNCCBgLgAKizW7DpgRUD3M9W9us2jWuVMEUXSr6pV3RBYpWN4597pnt~I~bEqs4Sl9RfKcbgo14hQ__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

Here, regarding our motors, consider the rotating shaft in the center, also called as a **rotor** in Figure 1 with a permanent magnet with 2 poles as your **donkey**, and consider the stationary part with the orange coils also called as a **stator** as your **carrot**. 

The orange coils on the stator work as an **electromagnet** that attracts the poles of the permanent magnets present in the rotor in-between the stator - see Figure 1. 

The rotor rotates whenever the electromagnets are switched on, and the magnets in-between move towards the electromagnets. 

Now, once the electromagnets attract the magnets on the rotor they need to change its polarity, to push the rotor forward along its rotational path so that it continues rotating, instead of getting stuck in one position. 

That is basically how a BLDC motor works.

We will learn in-depth about DC motors, BLDC motors and their control as well as building your own primitive motor from scratch in the EV 201 course.

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/4nhm4z3uak6wck6u50q8fke87tfv?response-content-disposition=inline%3B+filename%3D%22785px-Rotating-3-phase-magnetic-field.svg.png%22%3B&response-content-type=image%2Fpng&Expires=1719828680&Signature=kQaijQKkzSdWm6Ye26pMYfrg8kwExU0O3YSQIw6yfH5vSfSKQDtUYBcA04M3XUT-JDiwrYiMoDnQ6aj14K5jgT5P-DWZ6KAIGXpECqTmvhfqpcfnZTEZtC5K~qiTEbGugU-LHPHKHomFW9kqd1gTHfrpnww3wF3VMWQQZ2uCa3QywHJbzU~VdB~YXurGT6srpY1L6rjAWPO8L7MBBKmf~uGbRzzamEZj~TYdv6BXR6uudcTY-6qBStrNgaEcfSfLc4P9D471XUSPfI~ckrE8jHS~Un92W20BiL3QI4FGWHw9ixRUsyOopnge3gzaZyjhLQYV5bYgGyfPPNoZih27Iw__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

-=- *Rotating 3-phase magnetic field* | License:
[CC0 1.0 Universal Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/deed.en)

The arrow in the image above is the north pole of the magnet getting attracted towards the south pole of the constantly moving electromagnet.

Now that we have learned a bit about DC brushless motors, the next type is called an **induction motor**.

## A closer look at induction motor drives. 

A forerunner of the 3-phase induction motor was invented by Nikola Tesla sometime before 1889. Curiously, the stators for the 3-phase induction motor and the DC brushless motor are virtually identical. Both have three sets of “distributed windings” that are inserted within the stator core. The essential difference between the two machines is with the rotor.

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/g6ltjw3meq9prk2acrd93clw2n0j?response-content-disposition=inline%3B+filename%3D%22induction%2Bmotor.png%22%3B&response-content-type=image%2Fpng&Expires=1719828680&Signature=OhtmvXf~fyd9QBV~dJFkCj1Pil3eGMgIqKVeqy8d6lAWwLvjM5d0MKzvFt4i-jg~~uk~-p-SiiAu54mYZ2TLBCuwietFN-TsKe1I2UJySbeJMftG9wDTdCT7iBTtg79x2pee99vCl2P3H0Diw-dNyrBxHduxHlLPeVM3y5zEMS8fvWL7p8t4PglABz1kh8MIWGEavcJIjtHWBTDHIJbJAD6ys-zrC3Gv~fOLibGXZ3Vuib4QuWb~qtbzmQDYbRyq1Ca~Dbtg3dvJlra0bKq7yEqTveBxXHMrjIXoYXYqFn2yF5nsheTFGFAJVPKxX~Uo6UETBjf-~k5zd81EadxyiQ__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

-=- _Components of an induction motor_ | Source: [Robo Blazek](https://commons.wikimedia.org/wiki/File:AM_Klietka.png)

Lets, look at the different parts of the rotor of an induction motor, from the above image

1. **Shaft:** Connects the rotor to the output; this is the main component that transfers all the torque provided by the rotor to the outside load.

2. **Squirrel cage:** Named for its shape, it produces torque by interacting with the rotating magnetic fields.

<img class="mx-auto w-auto md:w-auto" alt="Rotating Magnetic Fields in an induction motor (The squirrel cage interacts with these fields and starts moving with them) just like how you move metal objects with a magnet" src="https://do7js0tdxrds1.cloudfront.net/2ziciqj4qj1aywr9l2ec4nuu861q?response-content-disposition=inline%3B+filename%3D%22Rotating_Magnetic_Field.gif%22%3B&response-content-type=image%2Fgif&Expires=1719828680&Signature=bt9ww87VjAcyxUY1vXU8S6zv65wZUBgX~m-1fbO72DwTrlIYWDujdtCDCw0Xs~uwyCrCzaZ7wgRFZS8-Zq8Wc6wC9J~MOt71tZElmphyLiEU~Q9yw1ZEpR241NCWzvE1a98H6WRA5~f7~WcfIt5KcVh4cviukdSipsz3pA5ZVdGAnqBRMblkDRtI6TvImfjQA2ruzWhXPpkxjDkb5ZxcvKTBl25zE7sD5hUZ-O5not3vi1fCtlLW7FTtM93MiExbZvn1xnqydMQKA6yS5XbCmJAOaOXNpTTW7NBqvAnJJJAemgDblIewzuNnKwsmaMvPcefxwKVPCWZjuzP38ZZnWA__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

-=- Credit: [el Fantin](https://commons.wikimedia.org/wiki/File:Rotating_Magnetic_Field.gif) | License:
[Creative Commons Attribution-Share Alike 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

3. **Laminations:** Help amplify the flux generated by the rotating magnetic fields, producing more adequate torque.

4. **Spline shaft:** A textured shaft that helps connect the laminations and the torque-producing components to the shaft.

As you can see, unlike the DC brushless rotor, the induction rotor has no magnets – just stacked steel laminations with buried peripheral conductors that form a “shorted structure.” Currents flowing in the stator windings produce a rotating magnetic field that enters the rotor. In turn, the frequency of this magnetic field as “seen” by the rotor is equal to the difference between the applied electrical frequency and the rotational “frequency” of the rotor itself. Accordingly, an induced voltage exists across the shorted structure that is proportionate to this speed difference between the rotor and electrical frequency. In response to this voltage, currents are produced within the rotor conductors that are approximately proportionate to the voltage, hence the speed difference. Finally, these currents interact with the original magnetic field to produce forces – a component of which is the desired rotor torque.

When a 3-phase induction motor is connected to utility type 3-phase power, torque is produced at the outset. 

The motor can start under load. No inverter is needed. The fact that induction motors are directly compatible with conventional utility power is the main reason for their success. In contrast, a brushless DC motor produces no starting torque when directly connected to fixed frequency utility power. They need the aid of an inverter whose “phase” is maintained in step with the angular position of the rotor.

## AC Induction Motor: To Choose or Not to Choose?
While 3-phase induction motors have great utility, they also have some severe limitations. They cannot operate from DC; AC is a must. Shaft speed is proportionate to line frequency. Hence, when used with utility power, they are constant-speed machines. Finally, when operated from utility power, they have limited starting torque and somewhat limited running peak torque capabilities, when compared to DC type machines.

Add an inverter (without any feedback control) and it becomes possible to power an induction machine from a battery or other DC source; variable speed also becomes possible simply by adjusting the inverter frequency. Still, torque performance is low compared with DC machines. Add some feedback loops such that the inverter produces the exact frequency that the motor “desires,” and the induction motor is now capable of competing with DC and DC brushless for vehicle applications.

<img class="mx-auto w-auto md:w-auto" alt src="https://do7js0tdxrds1.cloudfront.net/eo5gljxq8i75iws7dt8cvv0ldn9e?response-content-disposition=inline%3B+filename%3D%22final_60fac1f991d4b700978d36dd_783612.gif%22%3B&response-content-type=image%2Fgif&Expires=1693400456&Signature=U5IxfpRHNPgKtuYrxAgI5mE5ROaF2exjRBeIfbe0YMWFHYofmr1ozTo~ginzbwaaihgHEFUNoTb4tg8RpCJlfJZJZ36I28F75sqUI-U9ajqi44-L2hPRn8URX-Wck0OwZ1WVrjPaf2nEP5MmnWjZgUdE1qs7NxdfzSPEvHzzXMlXrqRQYnWvSjevdW2iNq-rnE9HPEAhuaCUSREwMSbD9t~6IeY03n~Qu8deVHzrYLKojFkIwtQw2g~zTKD5A3Pvvewh~YTX~6iSU9aoxVDNg491bg7l88XGxsIZ4rkdjm9k1RbOAZycXmbdga-KPX12Jxu2oFSFA5UyNSdanbqJ8Q__&Key-Pair-Id=K2Q3HDJ6ZAQGFF">

## Brushless or Induction?

Both DC brushless and induction drives use motors having similar stators. Both drives use 3-phase modulating inverters, with the primary differences being in the rotors and the inverter controls. With digital controllers, the control differences are mainly in the control code. (DC brushless drives require an absolute position sensor, while induction drives require only a speed sensor; these differences are relatively small.)

### Differences in Heat Generation and Efficiency

One of the main differences is that much less rotor heat is generated with the DC brushless drive. Rotor cooling is easier and peak point efficiency is generally higher for this drive. The DC brushless drive can also operate at unity power factor, whereas the best power factor for the induction drive is about 85 percent. This means that the peak point energy efficiency for a DC brushless drive will typically be a few percentage points higher than for an induction drive.

### In an ideal brushless drive

The strength of the magnetic field produced by the permanent magnets would be adjustable. When maximum torque is required, especially at low speeds, the magnetic field strength (B) should be maximum – so that inverter and motor currents are maintained at their lowest possible values. This minimizes the I²R (current² resistance) losses and thereby optimizes efficiency. Likewise, when torque levels are low, the B field should be reduced such that eddy and hysteresis losses due to B are also reduced. Ideally, B should be adjusted such that the sum of the eddy, hysteresis, and I² losses is minimized. 

Unfortunately, there is no easy way of changing "B" with permanent magnets.

### Induction Machines and Adjustable B Fields

In contrast, induction machines have no magnets and B fields are “adjustable,” since B is proportionate to V/f (voltage to frequency). This means that at light loads, the inverter can reduce voltage such that magnetic losses are reduced and efficiency is maximized. Thus, the induction machine when operated with a smart inverter has an advantage over a DC brushless machine – magnetic and conduction losses can be traded such that efficiency is optimized. This advantage becomes increasingly important as performance is increased. With DC brushless, as machine size grows, the magnetic losses increase proportionately and part load efficiency drops. With induction, as machine size grows, losses do not necessarily grow. Thus, induction drives may be the favored approach where high performance is desired; peak efficiency will be a little less than with DC brushless, but average efficiency may be better.

### Cost and Handling Considerations

Permanent magnets are expensive. Permanent magnet (PM) rotors are also difficult to handle due to large forces that come into play when anything ferromagnetic gets close to them. This means that induction motors will likely retain a cost advantage over PM machines. Also, due to the field weakening capabilities of induction machines, inverter ratings and costs appear to be lower, especially for high-performance drives. Since spinning induction machines produce little or no voltage when de-excited, they are easier to protect.

**I almost forgot:** Induction machines are more difficult to control. The control laws are more complex and difficult to understand. Achieving stability over the entire torque-speed range and over temperature is more difficult with induction than with DC brushless. This means added development costs, but likely little or no recurring costs.

## Let's recap

### 1. BLDC Motors:

#### Advantages:

- Generate much less heat compared to induction motors. 
- More powerful, with higher speed ranges, and higher dynamic responses. 
- These BLDC motors are therefore suitable for high-speed applications (10,000 rpm or above)
- Known for their excellent speed control.

#### Disadvantages:

- For bigger loads (industrial scale) an induction motor with inverter control will have better efficiency 
- Inverter electronics can be complicated and difficult to maintain in varied climatic conditions in India.


### 2. Induction Motors:

#### Advantages :
- Induction motors are robust and can operate in any environmental conditions, be it highly polluted or explosive environments.

- They are cheaper and nearly maintenance-free in cost due to the absence of brushes, slip rings, etc. In a non-inverter controlled induction motor, there are no electronics to worry about.

- If speed variation is not required, then induction motors can give better efficiency at peak load.

#### Disadvantages:
- Less efficient as compared to BLDC motors on average.
- Lower power factor and can at best give a power factor of 85% (or 0.85).
- Motion generates heat that can reduce the efficiency of the motor.

**Now that you know some basics of both the motors, you will be selecting the best type of motor for an electric vehicle in the next task.**