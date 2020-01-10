---
layout: post
title: From Proof of Concept to Prototype
bigimg: /img/20190815_181346.jpg
tags: [PPMM, pitch]
---

For many people I've talked with, it's not immediately clear what the proof of concept shows or why it is a guarantee that a prototype is possible. I'm going to explain that in this article.

## Essential principles

The ability to switch magnetic force is the basis of any motor using electromagnetism or magnetism. In electromagnetic motors, electric power converted into magnetic force in a coil is directly controlled by transistors, switches, or contacts. What is the strictly-magnetic equivalent of this?

It is far from obvious how a 'magnetic gate' could be created. A very simple thought demonstration that it is possible is the use of magnetic shielding via a mechanism partially made of an alloy with certain magnetochemical properties. Take for example, [mu-metal](https://en.wikipedia.org/wiki/Mu-metal), commonly found in hard drives. The strong magnets in hard drives will stick to a refrigerator with so much force, it is hard to remove them. Insert a piece of mu-metal between them and the force is effectively neutralized. A balanced 'modulating disc' having one half made of mu-metal and mounted on a small stepper motor can act as a magnetic gate, consuming very little power, because the magnetic field exerts no torque is exerted on the mu-metal modulator.

For anyone who has played with the innards of a destroyed hard drive, the effect is dramatic and its potential for doing work should be obvious.

The essential idea is to be able to shield, neutralize, or effectively 'turn off' the magnetic force of a strong magnet on demand. This must be done with precise timing, exactly as a converging magnet pair approach "top dead center" with respect to one another (to use a piston engine analogy). 

As the holding force is a normal force, not used in the action of the motor, the lateral forces are something  less, but not orders of magnitude less. In other geometries, the normal forces could be used. The ratio of the power input to rotate the modulating discs, overcoming the torque, in synchrony with moving magnet pairs (stator and rotor) simply must be far less than the impulse turning the rotor.  

This is not a 'perpetual motion,' 'overunity,' or 'free energy' device -- unless one considers a hydroelectric generator to be in that category. It is the Sun that ultimately drives a hydroelectric plant. What is the source of the magnet is a matter of speculation, but it is external to the system. The boundary of the closed system is far from intuitive.

The mu-metal modulator disk scenario is, I think, suboptimal due to the moment of inertia of the discs, which would put severe limits on the variability and maximum of rotor speed. It is only meant to serve as an analogy for the functioning of the Poly-Polar Magnet Motor. I could be wrong. It may turn out that the modulation disc concept will work better.

The PPMM concept relies on an effect similar to that of a [Halbach magnet array](https://en.wikipedia.org/wiki/Halbach_array) in which the arrangement and orientation of magnets 'engineer' a net magnetic force in desired directions, and are cancelled where not desired. This is again, only analogous to the behavior of quadripolar magnet pairs. Their mutual interactions are surprisingly counterintuitive and complex.

## Quadripolar magnet pair interactions

The quadripolar neodymium magnets instrumental to the Schürch Motor are somewhat enigmatic. They belong to a patented class of magnets with engineered field geometries. The pair used in my design have a useful "twist-release" effect and are currently used in high-end latches, twist-release utility belts, and science novelty toys. Engineers playing with them are consistently baffled by their unexpected behavior. 

A pair mechanically constrained coaxially will strongly attach --one cannot pull them apart by hand. I've tried to separate accidentally-joined magnets using vise-pliers and this destroyed the magnets. Yet, with a quarter-twist (that is possible to do by hand), the pair instantly and forcefully repel one another. The moment I first saw this, I reasoned that it was the basis of a new kind of high-efficiency motor.

With more degrees of freedom, the interactions of a quadripolar magnet pair are complex. Starting with a pair in a coaxial position, having a reasonable gap constraint of say, 1 mm, but free to move linearly along a coplanar track, they exhibit phases of attraction and repulsion along the track in short intervals. These phases can be modulated by rotating one mate of a pair with respect to the other mate. 

The possible variables are many, so I will start with describing the simplest starting condition: the axially-aligned postion.

When two mates are axially aligned and allowed to attract naturally, they also rotate to self-align at the same angle (I'll call this the 'zero' or 'top dead center' [TDC]) and have maximum normal attraction force, as a function of distance - determined by the mechanical gap constraint mentioned above. A rotor having such magnets embedded within has a minimum tolerance at which the force of the magnets can bend the rotor and 'crash' the magnets. A gap of 0.5 mm is at least a practical parameter. Closer tolerances have to withstand exponentially higher normal forces between magnets and involve expensive materials, and these costs must be balanced against the fact that the forces exploited are lateral and component forces, not the normal forces.

![graph of holding force v distance](/img/1122-force-v-distance.png)

A quarter turn of one mate in this configuration of linear freedom will result in a rapid release of attraction and reversal to repulsion. The field of repulsion is narrow, thus as the mate is pushed away, it soon enters another attraction phase, beginning at about one half the diameter of the magnet. A second quarter turn initiates another repulsion cycle, pushing it completely outside the diameter of its mate, whereupon the mutual influence again reverses to attraction but drops off sharply with distance so that it is negligible in comparison to another pair station coming into interaction at the same moment.

Each station under rotation phases can be considered a rapid series of attraction-repulsion impulses, playing out over the shared area of field influence of about 25 millimeters. These implulses effect a torque on the rotor.  

## The prototype

There is undoubtedly a net torque of the rotor ; the question to be answered then, is whether the net torque exceeds the sum of input torques required to rotate the magnets, under precise computer control. My experiments show that this is 'yes'  -- by a factor of perhaps 10 to 1. Sophisticated instruments will be needed to accurately measure this.

![graph of holding force v rotation](/img/1122-hold-v-rotation.png)

![graph of torque v rotation](/img/1122-torque-v-rotation.png)

Here according to the graphs, at 1.5mm gap, the ratio of maximum torque to maximum holding force is instructive: 

    28 N to 130 mNm   

I have estimated that to achieve the legal speed limit for bicycles in the USA, the sufficient maximum speed/torque ratio of the stepper motors is in the ball park of 20 Watts peak. The average power is probably in the area of 10 Watts. Then the amount of power obtainable from the rotor is a function of the average impulse force times the maximum switching rate. The switching rate depends on the quality of the stepper motors, of which there are a minimum of four. The reaction speed and mechanical durability of the stepper motors is critical.

The magnets have two equal field sides. Thus the rotor should interface with a stator array on both sides, neutralizing the net lateral stresses on the rotor, while doubling torque impulse forces on the rotor. This means the rotor could be made of a carbon reinforced 3D printed plastic, instead of machined aluminum. In this configuration, the total power per station required to overcome magnet pair torques will be double that of one side, thus peak impulse power consumption would be about 40 watts. 

The 20-millimeter diameter of the magnets establishes a harmonic relationship between their spacing, their number, and the radius of the station array from the hub. In the current design, the rotor has 15 magnets spaced apart 20 millimeters that interact with a minimum of four stator actuators. The magnet pair interactions occur in three half-steps spaced with one neutral half-step, resulting in a ratio of 4:5 (that is, 4 stator elements to 5 rotor elements). This is necessary to have control over the rotor's direction. This also means it is possible to have a maximum of 12 stator elements operating on 15 rotor elements, tripling the rotor torque (and tripling stator power consumption). 

This degree of complexity is not needed for a prototype, but could be worthwhile to maximize performance. Experimentation may also reveal that a less expensive ratio of 3:4 is possible, considering the complex dynamics of the attract-neutral-repel cycle, since their interaction track is in fact curved and not linear.

The rotor is sandwiched between two stator arrays and all are joined by two ball-bearing turntables. This is necessary to give maximum mechanical reinforcement to maintain gap tolerance at the perimeter where magnet pairs interact. The center of the rotor can key with MTB-type spline bike hubs, while its outer perimeter can be a ten inch chain sprocket, giving versatile drive options.

An Arduino microcontroller interfaces with optical position encoders on the rotor and each stator element's stepper motor. Experimentation will verify whether the Arduino is fast enough to compute real time for a realistic speed for bicyclists, but would undoubtedly be sufficient for a wheel chair. Higher performance could be obtained from a Raspberry Pi, but with the greater constant power cost. In either case, a Bluetooth Low Energy (BLE) interface provides wireless connectivity to crankshaft and throttle sensors and smartphone application interface, which provides for unlocking, monitoring, customization, and other functions. 

It should be feasible to mount batteries on one stator array, eliminating the need for coaxial power connectors or induction coils to power the station actuators and the microcontroller, but this will place a constraint on the maximum time between recharging. A small solar cell could theoretically power the system almost indefinitely.

## Software

Omitted from this discussion was the software needed to operate the motor system. Fortunately there are many development library options available to deal with stepper motor and sensor interfaces, wireless communications, physics, app server, and so on. This is a topic that will deserve its own focus at another time.




