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

## Operation:

AC Signal is applied on the first BJT, it appears in the amplified form across `Rc`. The second stage does further amplification.

## Advantages:
* Voltage amplification
* Excellent audio fidelity over a wide range of frequency [Large Band-width]
* Lower cost
* Circuit is very compact
* Excellent frequency response

## Disadvantages:
* Low power gain
* Becomes noisy as it is used
* Poor Impedance matching

**Note:** For even number of cascaded stages the output signal does not get inverted and vice versa.

# Transformer-Coupled Amplifier

## Operation:

When ac signal is applied to the base of first BJT. It appears in the amplified form across primary side of `TXF` then it goes from primary to secondary and further amplification is done by the second BJT.

## Advantages:
* No power is lost
* Excellent impedance matching
* Higher Gain for better impedance matching

## Disadvantages:
* Poor frequency response
* Very bulky and expensive
* Higher frequency distortion
* Tends to create whining sound at the output

## Application:
* Used for **`impedance matching`** 
* Used in **`loudspeaker`**

# Direct-Coupled Amplifier

## Operation:

If first stage uses `n-p-n` then second one uses `p-n-p` .. .. and so on.
The output from the collector of first BJT is fed to the input of second BJT.

## Advantages:
* Simple circuit arrangement
* Low cost

## Disadvantages:
* Can not be used amplifying high frequency
* Operation point is shifed due to temperature variations

## Application:
* Used at extremely low frequency signals e.g amplifying **`photo-electric current`**, **`thermo-couple`** current

# Comparison between multi-stage Amplifiers
| Particular  | RC        | TXF       | Direct   |
|-------------|-----------|-----------|----------|
| FR          | Excellent | Poor      | Best     |
| Cost        | Less      | More      | Least    |
| Imp Match   | Not Good  | Excellent | Good     |
| Use [ampli] | Voltage   | Power     | Low Freq |

# Feedback Amplifiers

# BASIC feedback Amplifier classification:
* VVT [Voltage Amplifier] ~ [In = V, Out = V]
* CCT [Current Amplifier] ~ [In = I, Out = I]
* VCT [Voltage to Current] ~ [In = V, Out = I] [AKA **Trans-Conductance Amplifier**]
* CVT [Current to Voltage] ~ [In = I, Out = V] [AKA **Trans-Resistance Amplifier**]
["T" = Transducer]

## Good to know:
* To maintain a stabilized feedback network, a source, basic amplifier, a load, sampling network and summing/comparison network are needed.

* To sample `VOLTAGE` the connection should be **`Parallel`** at output
* To sample `CURRENT` the connection should be **`Series`** at output

* To compare `VOLTAGE` the connection should be **`Series`** at input
* To compare `CURRENT` the connection should be **`Parallel`** at input

## Voltage to Voltage [VVT] Simple Model
![alt text](http://i.imgur.com/Uv5jG21.png)
### Ideal Condition:
R_in = infinity
R_out = 0
### Practical Condition:
Design the model such a way that,
R_in >> R_s
R_out << R_L


### Classification:
* Voltage Amplifier 
