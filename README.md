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
flowchart LR
    S1["<b>Stage 1: Classical ML</b><br/>Gas Turbine Ambient Derating<br/><i>(XGBoost / Compressor Physics)</i>"]
    S2["<b>Stage 2: Deep Time-Series</b><br/>Turbomachinery Degradation & RUL<br/><i>(Bi-LSTM / NASA C-MAPSS)</i>"]
    S3["<b>Stage 3: Dynamical Systems</b><br/>Rotor Dynamics & Vibration<br/><i>(SciPy RK45 / Neural ODE)</i>"]
    CAP1["<b>Capstone 1: Thermal PINN</b><br/>High-Temperature Heat Transfer<br/><i>(Pure PyTorch / Parameter Discovery)</i>"]
    CAP2["<b>Capstone 2: Reservoir PINN</b><br/>Two-Phase Buckley-Leverett Flow<br/><i>(Welge Shock Waves / Porosity Inversion)</i>"]

    S1 --> S2 --> S3 --> CAP1 & CAP2
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

---

## 🛠️ Technical Competencies & Tooling

<div align="center">

| Domain | Core Frameworks & Libraries |
|:---|:---|
| **Scientific Machine Learning (SciML)** | `PyTorch 2.x`, `Physics-Informed Neural Networks (PINNs)`, `Neural ODEs`, `Autograd` |
| **Statistical ML & Prognostics** | `Scikit-Learn`, `XGBoost`, `Pandas`, `NumPy`, `Bidirectional LSTM`, `Temporal Attention` |
| **Numerical Methods & Simulation** | `SciPy (solve_ivp, RK45)`, `Finite Difference Methods (Upwind, Crank-Nicolson)` |
| **Thermodynamics & Turbomachinery** | Brayton Cycle Derating, Jeffcott Rotordynamics, Hydrodynamic Bearings, NASA C-MAPSS |
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
└──────────────────────────────────────┴──────────────────────┴──────────────────────────┘
```

---

<p align="center">
  <i>"Combining fundamental physical conservation laws with modern differentiable architectures to advance energy systems engineering."</i>
</p>
