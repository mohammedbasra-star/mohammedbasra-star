# Mohammed Basra

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=1,11,21&height=210&section=header&text=Mohammed%20Basra&fontSize=48&fontColor=ffffff&animation=fadeIn&subtext=Scientific%20Machine%20Learning%20%7C%20Turbomachinery%20%7C%20Computational%20Physics&subfontSize=18&subfontColor=e0e0e0" width="100%"/>
</p>

<p align="center">
  <a href="https://github.com/mohammedbasra-star"><img src="https://img.shields.io/badge/GitHub-mohammedbasra--star-181717?style=for-the-badge&logo=github" alt="GitHub"/></a>
  <a href="mailto:mohammedbasra.star@gmail.com"><img src="https://img.shields.io/badge/Email-Contact%20Me-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Discipline-Scientific%20ML%20%26%20Energy-007ACC?style=for-the-badge" alt="Discipline"/>
  <img src="https://img.shields.io/badge/Frameworks-PyTorch%20%7C%20PINNs%20%7C%20Neural%20ODE-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="Frameworks"/>
</p>

---

## 🔬 About Me

I am a Mechanical Engineer and Scientific Machine Learning researcher specializing in the intersection of **Physics-Informed Deep Learning (PINNs)**, **Dynamical Systems**, and **Turbomachinery & Reservoir Dynamics**. 

My research bridges classical physical principles (Navier-Stokes, Buckley-Leverett porous media flow, Brayton thermodynamic cycles, and rotor vibration dynamics) with modern deep learning and neural differential equation solvers to enable high-accuracy predictive maintenance, physical parameter discovery, and real-time scientific simulation.

---

## 🚀 The Graduated Research Pathway (Scientific Machine Learning)

My academic repositories follow a **logically graduated progression** demonstrating continuous mastery from classical statistical thermofluid modeling to cutting-edge Physics-Informed Neural Networks:

```mermaid
flowchart TD
    S1["<b>Stage 1: Classical ML</b><br/>Gas Turbine Ambient Derating<br/><i>(XGBoost / Compressor Physics)</i>"]
    S2["<b>Stage 2: Deep Time-Series</b><br/>Turbomachinery Degradation & RUL<br/><i>(Bi-LSTM + Attention / C-MAPSS)</i>"]
    S3["<b>Stage 3: Dynamical Systems</b><br/>Rotor Dynamics & Bearing Instability<br/><i>(SciPy RK45 / Neural ODE)</i>"]
    
    subgraph CAP ["<b>Physics-Informed Deep Learning & Operator Learning (PINNs / FNO)</b>"]
        CAP1["<b>Thermal PINN</b><br/>2D High-Temp Conduction<br/><i>(Analytical & FDM Benchmark)</i>"]
        CAP2["<b>Reservoir PINN</b><br/>Buckley-Leverett Two-Phase Flow<br/><i>(Welge Shock Waves & Inversion)</i>"]
        CAP3["<b>Aerodynamics FNO</b><br/>Turbine Blade Transonic Flow<br/><i>(Continuous Operator Learning)</i>"]
        CAP4["<b>Combustion Neural ODE</b><br/>Stiff Chemical Kinetics & NOx<br/><i>(Arrhenius & Radau / BDF)</i>"]
        CAP5["<b>Conjugate Heat Transfer XPINN</b><br/>Blade Cooling & Multi-Domain CHT<br/><i>(Dual Subnet / Interface Jump)</i>"]
        CAP6["<b>Pump Cavitation FNO</b><br/>Rayleigh-Plesset Bubble Inception<br/><i>(Multiphase Spectral Operator)</i>"]
        CAP7["<b>Thermoacoustic PINN</b><br/>Combustion Humming & Rayleigh Criterion<br/><i>(Complex Helmholtz Eigenmodes)</i>"]
    end

    S1 --> S2 --> S3 --> CAP1 & CAP2 & CAP3 & CAP4 & CAP5 & CAP6 & CAP7
```

---

## 📂 Featured Research Repositories

### 1. [pinn-thermo-dynamics](https://github.com/mohammedbasra-star/pinn-thermo-dynamics)
**Physics-Informed Neural Network (PINN) for High-Temperature Turbomachinery Heat Transfer**
- Solves 2D nonlinear unsteady thermal conduction governed by $\rho c_p \frac{\partial T}{\partial t} = \nabla \cdot (k \nabla T) + Q$.
- Validated against $256 \times 256$ analytical and Crank-Nicolson numerical ground truth ($L_2 \text{ error} \approx 1.15 \times 10^{-4}$).
- Inverse parameter discovery of unknown thermal diffusivity $\alpha$ with $< 0.35\%$ error.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/pinn-thermo-dynamics/blob/main/notebooks/quickstart.ipynb)

### 2. [pinn-reservoir-dynamics](https://github.com/mohammedbasra-star/pinn-reservoir-dynamics)
**Physics-Informed Neural Network for Two-Phase Porous Media Flow & Buckley-Leverett Shock Waves**
- Solves nonlinear hyperbolic Buckley-Leverett saturation PDE with Welge fractional flow shock fronts: $\phi \frac{\partial S_w}{\partial t} + u_t \frac{\partial f_w}{\partial x} = 0$.
- Upwind Finite Difference numerical benchmark on $65,536$ spatiotemporal grid points.
- Inverse reservoir history matching for physical porosity discovery ($\phi \to 0.20$).
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/pinn-reservoir-dynamics/blob/main/notebooks/quickstart_reservoir_demo.ipynb)

### 3. [turbomachinery-rotor-dynamics-ode-](https://github.com/mohammedbasra-star/turbomachinery-rotor-dynamics-ode-)
**Dynamical Systems Modeling, 2-DOF Jeffcott Rotor with Duffing Stiffness, Capone Bearing Forces & Neural ODEs**
- High-fidelity formulation: 2-DOF rotor motion with nonlinear cubic Duffing stiffness and Capone hydrodynamic short-bearing Reynolds lubrication oil-film forces ($M \ddot{r} + C \dot{r} + K r + F_{\text{nl}}(r) = F_{\text{unbalance}}(t)$).
- Classical 4th/5th-order Runge-Kutta (SciPy RK45) ground truth vs continuous-time Neural ODE vs Collocation PINN baseline.
- Spectral analysis (FFT) tracking 1X synchronous unbalance ($50.0\text{ Hz}$ at $3000\text{ RPM}$) and subharmonic hydrodynamic oil whirl ($\sim 0.46\text{X}$).
- System identification discovering unbalance eccentricity ($e$) and bearing damping ($c$) from vibration orbits.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/turbomachinery-rotor-dynamics-ode-/blob/main/notebooks/quickstart_demo.ipynb)

### 4. [turbomachinery-degradation-lstm-](https://github.com/mohammedbasra-star/turbomachinery-degradation-lstm-)
**Deep Temporal Prognostics & Remaining Useful Life (RUL) on NASA C-MAPSS (BiLSTM + Temporal Attention)**
- Continuous degradation tracking across 100 aircraft turbofan engines with piecewise-linear RUL clipping ($RUL_{\max} = 125$).
- Bidirectional LSTM with Multi-Head Temporal Self-Attention and robust Huber loss for early degradation anomaly detection.
- Achieved test benchmark of **$\text{RMSE} = 9.76\text{ cycles}$** and **NASA Score $S = 158.0$**, significantly outperforming standard regressors.
- Explainability heatmaps visualizing temporal attention weights across operational sensor sequences.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/turbomachinery-degradation-lstm-/blob/main/notebooks/rul_quickstart_demo.ipynb)

### 5. [gas-turbine-ambient-effects-regression-](https://github.com/mohammedbasra-star/gas-turbine-ambient-effects-regression-)
**Machine Learning Benchmark for Gas Turbine Power Derating Under Ambient Climatic Effects**
- Brayton cycle thermodynamic derating analysis ($T_{amb}, P_{amb}, RH, V$) based on compressor air density loss ($\dot{m} = \rho A v$).
- Benchmark suite of 5 models trained on 9,568 full-load hourly observations (UCI CCPP).
- Tuned XGBoost achieved **$R^2 = 0.9610$** and **$\text{RMSE} = 3.364\text{ MW}$** ($0.56\%$ MAPE).
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/gas-turbine-ambient-effects-regression-/blob/main/notebooks/quickstart_demo.ipynb)

### 6. [turbine-blade-aerodynamics-fno-](https://github.com/mohammedbasra-star/turbine-blade-aerodynamics-fno-)
**Turbine Blade Aerodynamics with 2D Fourier Neural Operators (FNO)**
- Continuous operator mapping ($\mathcal{G}_\theta : \mathcal{A} \to \mathcal{U}$) from blade geometry SDF and freestream Mach $M_\infty$ to complete velocity $(u, v)$ and pressure $C_p$ fields.
- 4-layer 2D Spectral Convolution kernel operating directly in frequency domain (`torch.fft.rfft2`).
- Real-time surrogate inference ($< 4\text{ ms}$) achieving **$50,000\times$ speedup** over classical compressible CFD solvers.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/turbine-blade-aerodynamics-fno-/blob/main/notebooks/quickstart_demo.ipynb)

### 7. [gas-turbine-combustion-kinetics-node-](https://github.com/mohammedbasra-star/gas-turbine-combustion-kinetics-node-)
**Gas Turbine Combustion Kinetics & Thermal NOx with Stiff Neural ODEs**
- Stiff ODE modeling of multi-step Arrhenius chemical kinetics and autoignition thermal runaway across $P \in [10, 25]\text{ bar}$.
- Resolves extreme chemical stiffness ($\text{ratio } > 10^5$) and predicts thermal $NO_x$ formation via the extended Zeldovich mechanism.
- Physical element conservation (C, H, O, N) and total mass fraction constraint ($\sum Y_k = 1.0$) embedded in loss formulation.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/gas-turbine-combustion-kinetics-node-/blob/main/notebooks/quickstart_demo.ipynb)

### 8. [heat-exchanger-conjugate-xpinn-](https://github.com/mohammedbasra-star/heat-exchanger-conjugate-xpinn-)
**Conjugate Heat Transfer (CHT) with Extended PINNs (XPINNs)**
- Multi-domain physics modeling coupled solid metal conduction ($\nabla^2 T_s = 0$) and laminar fluid convection ($u \partial_x T_f - \frac{1}{\text{Pe}} \nabla^2 T_f = 0$).
- Dual-subnet architecture capturing the sharp normal temperature gradient slope jump ($k_s/k_f = 10$) where monolithic PINNs fail.
- Rigorous verification against Finite Volume ground truth ($> 3\times$ higher accuracy than single-network PINNs).
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/heat-exchanger-conjugate-xpinn-/blob/main/notebooks/quickstart_demo.ipynb)

### 9. [basra-extreme-heat-turbine-derating-ml--](https://github.com/mohammedbasra-star/basra-extreme-heat-turbine-derating-ml--)
**Gas Turbine Derating in Extreme Summer Heat (>50°C) — Basra, Southern Iraq**
- Models compressor air density loss ($\dot{m} = \rho A v$) and Brayton cycle net power collapse under extreme heat ($> 50^\circ\text{C}$) in Shatt Al-Basra / Rumaila.
- Physics-Guided MLP enforcing thermodynamic monotonicity constraint ($\partial P / \partial T_{amb} \le 0$) on 8,760 hourly Basra meteorological records.
- Evaluates evaporative fogging inlet air chilling, identifying up to $+14.7\text{ MW}$ power recovery potential.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/basra-extreme-heat-turbine-derating-ml--/blob/main/notebooks/quickstart_demo.ipynb)

### 10. [iraqi-dust-storm-blade-erosion-pinn--](https://github.com/mohammedbasra-star/iraqi-dust-storm-blade-erosion-pinn--)
**Compressor Blade Abrasive Erosion Under Iraqi Summer Dust Storms (Shamal Winds)**
- Eulerian-Lagrangian drag dynamics and Stokes particle tracking of airborne quartz sand ($d_{mean} \approx 18\mu\text{m}$, Rosin-Rammler spectrum).
- PINN models particle velocity field $(u_p, v_p)$ and predicts leading-edge metal mass removal via Tabakoff & Grant erosion law.
- Pinpoints severe erosion concentration zones on compressor blade leading edge and pressure shoulders.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/iraqi-dust-storm-blade-erosion-pinn--/blob/main/notebooks/quickstart_demo.ipynb)

### 11. [iraqi-desert-solar-pv-dust-thermal-ml--](https://github.com/mohammedbasra-star/iraqi-desert-solar-pv-dust-thermal-ml--)
**Desert Solar PV Thermal Degradation & Dust Soiling Optimization — Ar-Ratawi, Basra**
- Coupled thermal-dust modeling for utility-scale desert solar farms: cell overheating beyond $72^\circ\text{C}$ ($\gamma_P \approx -0.38\%/\text{K}$) and optical Beer-Lambert dust attenuation.
- Physics-guided multi-target ML predicting cell temperature ($R^2 = 0.9999$) and actual generation ($R^2 = 0.9982$).
- Optimizes automated water-free robotic dry-cleaning schedule, recovering $+\$1.85\text{ Million}$ annually per 100 MW block.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/iraqi-desert-solar-pv-dust-thermal-ml--/blob/main/notebooks/quickstart_demo.ipynb)

### 12. [centrifugal-pump-cavitation-fno](https://github.com/mohammedbasra-star/centrifugal-pump-cavitation-fno)
**Cavitation Inception & Rayleigh-Plesset Bubble Dynamics in Centrifugal Pumps using 2D Fourier Neural Operators**
- Non-equilibrium vapor bubble explosive growth and collapse shockwaves governed by the generalized Rayleigh-Plesset ODE.
- Euler turbomachinery head, Wiesner slip factor, and Net Positive Suction Head Available vs Required ($\text{NPSH}_A \le \text{NPSH}_{3\%}$) 3% head breakdown.
- 2D Fourier Neural Operator (`FNO2d`) mapping impeller conformal geometry and flow coefficient to 2D static pressure and vapor volume fraction $\alpha_v(x, y)$ ($15,000\times$ speedup over multiphase VOF CFD).
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/centrifugal-pump-cavitation-fno/blob/main/notebooks/quickstart_demo.ipynb)

### 13. [thermoacoustic-instability-helmholtz-pinn](https://github.com/mohammedbasra-star/thermoacoustic-instability-helmholtz-pinn)
**Combustion Humming, Flame-Acoustic Coupling, and Rayleigh Criterion with Complex-Valued PINNs**
- Inhomogeneous Helmholtz wave equation with $n$-$\tau$ flame transfer function (FTF) predicting complex resonant acoustic eigenfrequencies $\omega = \omega_r + i \sigma$.
- Dual-head Complex-PINN solving real and imaginary acoustic pressure mode shapes $\text{Re}(\hat{p}), \text{Im}(\hat{p})$ in gas turbine can-annular combustors ($0.003\%$ frequency discrepancy vs analytical acoustic theory).
- Rayleigh criterion energy budget evaluation mapping driving vs damping zones and establishing neutral stability boundaries ($\sigma = 0$) in $(n_f, \tau)$ parameter space.
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mohammedbasra-star/thermoacoustic-instability-helmholtz-pinn/blob/main/notebooks/quickstart_demo.ipynb)

---

## 🛠️ Technical Competencies & Tooling

<div align="center">

| Domain | Core Frameworks & Libraries |
|:---|:---|
| **Scientific Machine Learning (SciML)** | `PyTorch 2.x`, `Fourier Neural Operators (FNO)`, `Complex-PINNs`, `Neural ODEs`, `Autograd` |
| **Statistical ML & Prognostics** | `Scikit-Learn`, `XGBoost`, `Pandas`, `NumPy`, `Bidirectional LSTM`, `Temporal Attention` |
| **Numerical Methods & Simulation** | `SciPy (solve_ivp, RK45)`, `Finite Difference Methods (Upwind, Crank-Nicolson)` |
| **Thermodynamics & Turbomachinery** | Brayton Cycle Derating, Centrifugal Pump Cavitation, Combustor Acoustics, Rotordynamics |
| **Data Visualization & Publishing** | `Matplotlib`, `Seaborn`, `Publication 300 DPI Graphics`, `LaTeX (KaTeX)` |

</div>

---

## 📊 Summary of Research Performance Metrics

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│  PROJECT BENCHMARK PERFORMANCE DASHBOARD                                               │
├──────────────────────────────────────┬──────────────────────┬──────────────────────────┤
│  Repository                          │  Primary Metric      │  Verification Benchmark  │
├──────────────────────────────────────┼──────────────────────┼──────────────────────────┤
│  pinn-thermo-dynamics                │  L2 Error = 1.15e-4  │  Analytical 256x256 Grid │
│  pinn-reservoir-dynamics             │  L2 Error = 4.21e-3  │  Upwind FDM Shock Front  │
│  turbomachinery-rotor-dynamics-ode   │  MSE Loss = 5.50e-10 │  RK45 Numerical Solver   │
│  turbomachinery-degradation-lstm     │  Test RMSE = 9.76 cy │  NASA C-MAPSS Fleet (100)│
│  gas-turbine-ambient-effects-regression│ R² Score = 0.9610   │  UCI CCPP (9,568 Points) │
│  turbine-blade-aerodynamics-fno      │  Speedup = 50,000x   │  Compressible CFD Flow   │
│  gas-turbine-combustion-kinetics-node│  Stiffness > 10^5    │  Radau / BDF Chemistry   │
│  heat-exchanger-conjugate-xpinn      │  L2 Error = 1.12e-1  │  FVM Multi-Domain Solver │
│  basra-extreme-heat-turbine-derating-ml│ R² Score = 0.9982   │  8,760h Basra Climate    │
│  iraqi-dust-storm-blade-erosion-pinn │  Erosion MSE = 4.1e-4│  Tabakoff & Shamal Dust  │
│  iraqi-desert-solar-pv-dust-thermal-ml│ R² Score = 0.9982   │  Ar-Ratawi 1 GW Desert PV│
│  centrifugal-pump-cavitation-fno     │  Rel L2 = 5.75%      │  Multiphase VOF Solver   │
│  thermoacoustic-instability-helmholtz│  Freq Err = 0.003%   │  Acoustic Resonant Theory│
└──────────────────────────────────────┴──────────────────────┴──────────────────────────┘
```

---

<p align="center">
  <i>"Combining fundamental physical conservation laws with modern differentiable architectures to advance energy systems engineering."</i>
</p>
