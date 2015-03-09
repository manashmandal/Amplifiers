# Multi-Stage Amplifiers

* In `RC` Coupling, a capacitor is used as the coupling device. The capacitor connects the output of one stage to the input of the next stage in order to pass the `AC` Signal on while `BLOCKING DC BIAS VOLTAGE`. 
* In `Transformer` Coupling, transformer is used as the coupling device. It performs same actions as RC Coupled amplifier but permits `IMPEDANCE MATCHING`.
* In `Direct Coupling` the individual amplifier stage bias condition are so designed that the two stages may be directly connected without the necessity for `DC ISOLATION`.

## Why `CAPACITORS` are used?

Capacitors serve the following two roles in `BJT`
* As **`COUPLING`** Capacitor
* As **`BYPASS`** Capacitor 

### **Coupling** Function:
* It blocks DC and provides **`isolation between AC and DC`**
* It passes `AC` signal from one stage to the next stage with **`little or no distortion`**

### **Bypass** Function:
* Bypass capacitor also blocks dc but it is connected to **`Emitter-Ground`** junction `And Parallel to Re` so the AC signal passes from base to Ground without passing through `Re` as Re never existed in the first place.
* It also **`INCREASES VOLTAGE GAIN`**, if bypass capacitor is not used then gain can be sharply reduced.

## Important Terms and Definitions:
* **Gain:** The ratio of output electrical quantity to input electrical quantity.
* **Frequency Response:** The gain of amplifier varies with signal frequency, **`The curve between voltage gain and signal frequency`**

# R-C Coupled Transistor Amplifier

## Advantages:
* Voltage amplification
* Excellent audio fidelity over a wide range of frequency [Large Band-width]
* Lower cost
* Circuit is very compact
* Excellent frequency response

## Disadvantages:
