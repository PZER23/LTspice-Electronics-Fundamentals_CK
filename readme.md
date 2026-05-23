# Exercise 01: Ohm's Law & Power Dissipation

## 1. Objective
The purpose of these foundational exercises is to : 
Understanding Ohm's law and the relationship between voltage, current, and resistance(EXERCICE_1)
Understanding the effect of resistance value on current and power dissipation(EXERCICE_2)
Understanding a series circuit(EXERCICE_3)

## 2. Circuit Schematic (LTspice)
![Circuit Schematic1](./Analysis_of_a_simple_resistive_circuit_SCHEMA.png)
![Circuit Schematic2](./The_influence_of_the_resistance_on_the_current_SCHEMA.png)
![Circuit Schematic2](./Voltage_division_in_a_series_circuits_SCHEMA.png)

## 3. Theoretical Analysis
EXERCICE 1
Using a DC voltage source of **9 V** and a resistor of **2000 Omega**, the mathematical expectations are:
* Current ($I$): $I = \frac{V}{R}$ = \frac{9\text{V}}{2000\ \Omega} = 4.5\text{ mA}$
* Power Dissipation ($P$): $P = V \cdot I = 9\text{V} \cdot 0.0045\text{A} = 40.5\text{ mW}$
---
EXERCICE 2
Using a DC voltage source of **12 V** and many resistor **R1 = 10 000 Omega**, **R2 = 1000 Omega**, **10 Omega**, the mathematical expectations are:
* Current ($I$): $I = \frac{V}{R}$ . $I_1 = 1.2\text{ mA}$, $I_2 = 12\text{ mA}$, $I_3 = 120\text{ mA}$ .
* Power Dissipation ($P$): $P = V \cdot I$ .  $P_1 = 14.4\text{ mW}$, $P_2 = 144\text{ mW}$, $P_3 = 1440\text{ mW}$
---
EXERCICE 3
Using a DC voltage source of **12 V** and two resistor **R1 = 1000 Omega**, **R2 = 2000 Omega**, the mathematical expectations are:
* Equivalent resistance ($R_{eq}$): $R_{eq} = R_1 + R_2 = 3000 Omega .
* Current ($I$): $I = \frac{V}{R{eq}}$ = \frac{12\text{V}}{3000\ \Omega} = 4\text{ mA}$
* Voltage ($V$): $V = R \cdot I$ .  $V_1 = 4\text{V}$, $V_2 = 8\text{V}$
* Power Dissipation ($P$): $P = V \cdot I$ .  $P_1 = 16\text{ mW}$, $P_2 = 32\text{ mW}$
    
## 4. Simulation Results & Comparison

The circuit was simulated using the operating point directive (`.op`) in LTspice.

EXERCICE 1

![Simulation Results](./Simulation_resuts_1.png)


| Electrical Parameter | Theoretical Value | Simulated Value | Discrepancy (%) |
| :--- | :---: | :---: | :---: |
| Loop Current ($I$) | 4.5 mA | 4.5 mA | 0% |
| Power Dissipation ($P$) | 0.0405 W | 40.499998 mW | 0% |

EXERCICE 2

![Simulation Results](./Simulation_resuts_2.png)


| Electrical Parameter | Theoretical Value | Simulated Value | Discrepancy (%) |
| :--- | :---: | :---: | :---: |
| Loop Current ($I$) | 4.5 mA | 4.5 mA | 0% |
| Power Dissipation ($P$) | 0.0405 W | 40.499998 mW | 0% |

## 5. Technical Insights
The simulation matches the mathematical calculations perfectly (0% error). This confirms the validity of the simulator's internal solver for basic DC operations and establishes the baseline methodology for upcoming complex networks.
