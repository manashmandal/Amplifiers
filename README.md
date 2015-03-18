# Multi-Stage Amplifiers

* In `RC` Coupling, a capacitor is used as the coupling device. The capacitor connects the output of one stage to the input of the next stage in order to pass the `AC` Signal on while `BLOCKING DC BIAS VOLTAGE`. 
* In `Transformer` Coupling, transformer is used as the coupling device. It performs same actions as RC Coupled amplifier but permits `IMPEDANCE MATCHING`. Usually a `STEP DOWN` Transformer is used for higher current output.
* In `Direct Coupling` the individual amplifier stage bias condition are designed such a way that the two stages may be directly connected without the necessity for `DC ISOLATION`.

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
* It reduces `Stability`

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
* Higher Gain for better impedance matching [Matches `HIGH OUTPUT IMPEDANCE` of `first stage` and `LOW INPUT IMPEDANCE` of the second stage] 
* Voltage drop is less of a transformer winding than a collector resistor.

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

**Note: `Excellent` is better than `Best`** 

# Feedback Amplifiers

# BASIC feedback Amplifier classification:
* VVT [Voltage Amplifier] ~ [In = V, Out = V]
* CCT [Current Amplifier] ~ [In = I, Out = I]
* VCT [Voltage to Current] ~ [In = V, Out = I] [AKA **Trans-Conductance Amplifier**]
* CVT [Current to Voltage] ~ [In = I, Out = V] [AKA **Trans-Resistance Amplifier**]

["T" = Transducer]

## Good to know:
* To maintain a stabilized feedback network, a source, basic amplifier, a load, sampling network and summing/comparison network are needed.

* To sample `VOLTAGE` the connection should be **`Parallel`** / **`Shunt`** at output
* To sample `CURRENT` the connection should be **`Series`** at output

* To compare `VOLTAGE` the connection should be **`Series`** at input
* To compare `CURRENT` the connection should be **`Parallel`** / **`Shunt`** at input

## Voltage to Voltage [VVT] Simple Model [AKA **`Voltage-Series`**]

![alt text](http://i.imgur.com/Uv5jG21.png)

### Ideal Condition:

R_in = infinity

R_out = 0

### Practical Condition:

Design the model such a way that,

R_in >> R_s

R_out << R_L

### Phase Shift:

## Current to Current [CCT] Simple Model  [AKA **`Current-Shunt`**]
![alt text](http://i.imgur.com/RUwXrtx.png)

### Condition:

R_in << R_s

R_out >> R_L

### Phase Shift:

## Voltage to Current [VCT] Simple Model [AKA **`Current-Series`**]

![alt text](http://i.imgur.com/kiCYrEa.jpg)

## Condition:

R_i >> R_s

R_L << R_o

### Phase Shift:

## Current to Voltage [CVT] Simple Model [AKA **`Voltage-Shunt`**]

![alt text](http://i.imgur.com/xfsxM7K.jpg)

## Condition:

R_i << R_s

R_o << R_L

### Phase shift: 

# Why Feedback Amplifiers are used?

> A negative feedback amplifier (or more commonly simply a feedback amplifier) is an amplifier a fraction of the output of which is combined with the input so that a negative feedback **opposes** the original signal. **`The applied negative feedback improves performance (gain stability, linearity, frequency response, step response) and reduces sensitivity to parameter`** variations due to manufacturing or environment. Because of these advantages, negative feedback is used in this way in many amplifiers and control systems.

# Push-Pull Power Amplifier

## Difference between `VOLTAGE` and `POWER` Amplifier:

| Voltage Amplifier               | Power Amplifier                              |
|---------------------------------|----------------------------------------------|
| High valued 'beta' so base thin | Base is made thicker to handle large current |
| Usually R-C coupling            | Mostly TXF coupling                          |
| Input voltage: LOW              | HIGH                                         |
| Power output LOW                | HIGH                                         |
| Output impedance HIGH           | LOW                                          |

## Classification of Power Amplifiers:

### Class A: 
* Collector current flows at all times during the full cycle of signal.
* Impedance matched to supply full power at output
* Output wave is exactly similar as input
* Low power output and low collector efficiency

### Class B:
* Collector current flows only during the positive half cycle of the input signal.
* Higher power Output packed with higher efficiency
* Mostly push-pull arranged

### Class C:
* Collector current flows for less than half cycle of the input signal.
* Never used for power amplification
* Used as tuned amplifiers to amplify narrow band of frequencies.

## Comparison of Amplifier Classes

|                          | A       | AB       | B     | C     | D                  |
|--------------------------|---------|----------|-------|-------|--------------------|
| Operating Cycle [degree] | 360     | 180~360  | 180   | < 180 | Pulse Operation    |
| Power efficiency         | 25%~50% | 25~78.5% | 78.5% |       | Typically over 90% |




# JFET voltage amplifier

The JFET equivalents of BJT configurations are:
* Common Source -> CE
* Common Gate -> CB
* Common Drain [AKA Source follower] -> CC 

## Example of Common Source Config
![alt text](http://i.imgur.com/BwLLayi.png)

* Cs bypass capacitor grounds source for AC. Hence C1 and C0 Coupling capacitors phase inversion 180 Degree input to output.
* Provides high voltage and power gain
* Unstable current gain

> * Gate of JFET returned to ground through R0
> * As current flows through Rs it places a positive voltage on the gate. The reverse biases the Gs junction required for opeation
> * Gate has no loading effect on source since R0 provides ground
> * As the input (Gate) varies the output changes across Rd


# Op-Amp [Operational Amplifier]
If following waveshapes pass through **Differentiator** then the output will be

![alt text](http://i.imgur.com/VL5q8bM.gif)

// **Author: Manash** //

// Document Shortlink: `http://bitly.com/amplifierz` //
