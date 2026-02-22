# Two‑Compartment IV Bolus Model – MATLAB

This project simulates drug concentration over time after an intravenous (IV) bolus dose using a two‑compartment pharmacokinetic model. The code consists of a driver script (which sets parameters and solves the ODEs) and a separate function defining the differential equations.

## What I Built

- **Two‑compartment PK model**:
  - Central compartment (volume `V1`, elimination rate constant `k10 = CL/V1`)
  - Peripheral compartment (volume `V2`, inter‑compartment rate constants `k12` and `k21` based on inter‑compartmental clearance `Q`)
- **IV bolus dose**: Initial amount in the central compartment = `D` (dose), peripheral compartment starts at zero.
- **ODE system**:
  - `dA1/dt = -(k10 + k12)*A1 + k21*A2`
  - `dA2/dt = k12*A1 - k21*A2`
- **Numerical solution**: MATLAB’s `ode23` (or `ode45`) solves the system.
- **Visualization**: Two subplots – linear and semi‑log concentration‑time profiles.

<img width="560" height="338" alt="image" src="https://github.com/user-attachments/assets/692703b7-e8a0-460b-9adc-ecfe41fda1b2" /><img width="560" height="338" alt="image" src="https://github.com/user-attachments/assets/1f6a0be2-5b0b-4992-93fe-43c8a7615175" />



## Skills Demonstrated

- MATLAB programming (scripting, function definition, ODE solvers)
- Pharmacokinetic modeling (two‑compartment, IV bolus)
- Numerical solution of differential equations (`ode23`, `deval`)
- Parameter handling (passing extra parameters to ODE functions)
- Data visualization (subplots, linear and semi‑log scales)

## How to Run

1. Ensure both the driver script and the function `WK3_Class_4_101` are in the same folder (or on your MATLAB path).
2. Open the driver script (e.g., `TwoComp_Bolus_Driver.m`) in MATLAB.
3. Modify parameters at the top of the script (`D`, `V1`, `CL`, `Q`, `V2`) as desired.
4. Click **Run** or type the filename in the Command Window.

**Note**: The driver script currently contains commented code and multiple sections. For a clean run, uncomment the relevant parts and make sure the function name matches. A self‑contained example is provided below.

