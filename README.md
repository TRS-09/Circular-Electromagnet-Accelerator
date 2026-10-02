# Circular-Electromagnet-Accelerator
A circular track that uses four electromagnetic coils and optical light gates to accelerate a steel ball bearing around the track. Each light gate detects the position of the ball and triggers the next coil, creating a sequence of acceleration stages.

# **Further explanation**
The track is circular and consists of four electromagnetic coils which are used to accelerate a steel ball bearing as it goes around the track; the ball is detected by optical sensors, and as the ball passes each sensor, that sensor activates the following coil.

The system is set up in such a way that the ball is able to keep circulating around the track, going through a number of acceleration stages.

## How it works

The circular path has four coils placed around it.

When the ball comes near a coil, an LED and a photodiode detect its position; the photodiode is included in a voltage divider and thus produces a voltage that varies whenever the ball interrupts the light.

It is used in order to control the MOSFETs which switch on the relevant coil.

A magnetic field is produced by the coil and this causes the ball to accelerate. When the ball has reached the proper position, the coil is switched off so that the ball is not greatly slowed down by the magnetic field.

As the ball goes around the track, the four stages carry on repeating.

## Ball material

The ball should be constructed using soft iron or some other appropriate low-retentivity ferromagnetic material.

It is important since the ball must be strongly attracted to the electromagnetic coils when the coils are energised, but should almost lose all of its magnetisation when the magnetic field is switched off.

A ball that has been permanently magnetised would continue to be attracted to the coils after they have been switched off, which would decrease the acceleration and might prevent the ball from circulating properly.

## Coil drivers

The two IRLZ44N MOSFETs are used to switch each coil.

Since the coils draw about 10 A during an acceleration pulse, heatsinks are fitted to the MOSFETs in order to reduce heat buildup during operation.

The capacitors, which are placed near the coil drivers, supply the large current needed for the pulses since it is not necessary for the battery and the wiring to provide all of the energy for the pulse at once.

## Optical sensors

Each acceleration stage has its own optical sensor consisting of:

* LED
* Photodiode
* Resistors
* Voltage divider
* MOSFET switching circuit

The photodiode picks up any changes in the light that reaches the sensor; this in turn causes a change in the voltage across the resistor network, which is then used to switch on the MOSFETs that control the coil.

The coils can then be triggered automatically in accordance with the position of the ball instead of relying on a mechanical switch or a microcontroller.

## Power system

The system makes use of a 2S2P configuration of 18650 lithium-ion cells.

The battery system is linked to a charging/protection board so that the cells can be charged and controlled as a pack.

Capacitors are similarly used in the power system to produce the high-current pulses needed by the coils.

## Cooling

The current needed during operation is managed by two MOSFETs in each coil.

Heatsinks are attached to the MOSFETs in order to keep their operating temperature low and to avoid excessive heating during repeated acceleration cycles.

## Main features

* Circular recirculating track
* Four electromagnetic acceleration stages
* Optical triggering using LEDs and photodiodes
* Automatic coil switching
* IRLZ44N MOSFET coil drivers
* Approximately 10 A coil current
* Two MOSFETs per coil
* Heatsinks for the MOSFETs
* Capacitor-assisted high-current pulses
* 2S2P 18650 battery pack
* Integrated charging/protection board
* No microcontroller required for coil triggering
* Requires a soft iron/low-retentivity ball

## Design

The system was created with the aim of examining electromagnetic acceleration as well as the practical problems associated with switching high-current inductive loads.

The project involves electromagnetic induction, transistor switching, optical sensing, energy storage, battery systems and mechanical design.

Because of its circular design the ball is able to go through the four acceleration stages repeatedly instead of needing a long straight track.
