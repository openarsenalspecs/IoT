# ForwardState

**Holding Balance Before It Drifts.**

ForwardState is a modular predictive control and state-estimation platform designed to provide the software intelligence layer for cryogenic propellant conditioning, transfer, and in-space refueling systems.

ForwardState continuously evaluates the current and predicted state of a physical system, identifies developing instability, and determines control actions before the system moves outside its desired operating envelope.

ForwardState is designed to operate alongside [PhaseLock](https://gitlab.com/Roxanne_Ardary/phaselock). PhaseLock provides the physical cryogenic conditioning and transfer infrastructure, while ForwardState provides predictive state estimation, control, simulation, anomaly detection, optimization, and operational intelligence.

The architecture is designed to be modular, hardware-independent, locally operable, fault-tolerant, and extensible through optional plugins.

---

# Project Goals

ForwardState is designed to:

- Predict system behavior before instability occurs.
- Maintain a continuously updated system state.
- Fuse data from multiple sensors.
- Estimate states that cannot be directly measured.
- Predict temperature, pressure, flow, and phase behavior.
- Coordinate physical control systems.
- Provide model predictive control.
- Detect developing anomalies.
- Identify sensor and actuator failures.
- Coordinate with PhaseLock.
- Support digital-twin simulation.
- Support hardware-in-the-loop testing.
- Optimize transfer operations.
- Coordinate multiple tanks and vehicles.
- Support autonomous operations with human oversight.
- Provide deterministic safety boundaries around adaptive systems.
- Operate locally without mandatory cloud connectivity.
- Support different spacecraft, depots, hardware configurations, and mission architectures.

---

# System Architecture

ForwardState uses a layered modular architecture.

### Core System

The Core System provides the runtime, state model, configuration, communication, safety boundaries, and module-management infrastructure.

### Core Modules

Core modules provide the fundamental predictive-control capabilities required for ForwardState operation.

### Optional Plugin Modules

Plugins provide specialized capabilities that are not required by every deployment.

Plugins can be installed, removed, upgraded, or disabled without redesigning the Core System.

### External Systems

ForwardState can integrate with:

- PhaseLock
- Spacecraft flight computers
- Orbital propellant depots
- Ground systems
- Digital twins
- Simulation platforms
- Mission-control systems
- Telemetry networks
- Engineering databases

---

# Core Modules

## Runtime Module

The Runtime Module provides the execution environment for ForwardState.

Capabilities include:

- Module lifecycle management.
- Scheduling.
- Event processing.
- Configuration loading.
- Runtime state management.
- Health monitoring.
- Fault handling.
- Resource management.
- Plugin management.
- Process supervision.
- Deterministic execution modes.
- Local operation.

The Runtime Module provides the foundation on which all other ForwardState components operate.

---

## State Estimation Module

The State Estimation Module maintains the current estimated state of the physical system.

Capabilities include:

- Sensor fusion.
- State reconstruction.
- Noise filtering.
- Sensor validation.
- State confidence estimation.
- Missing-data handling.
- Outlier rejection.
- Redundant-sensor comparison.
- State-history tracking.
- State uncertainty estimation.

The state estimator can combine measured and inferred information into a unified system state.

---

## Sensor Fusion Module

The Sensor Fusion Module normalizes information from heterogeneous sensors.

Supported inputs may include:

- Temperature.
- Pressure.
- Differential pressure.
- Flow.
- Mass flow.
- Tank level.
- Density.
- Acceleration.
- Vibration.
- Valve position.
- Pump state.
- Thermal measurements.
- Leak sensors.

Capabilities include:

- Sensor normalization.
- Calibration handling.
- Timestamp synchronization.
- Sensor confidence scoring.
- Redundant sensor comparison.
- Sensor drift detection.
- Sensor failure detection.
- Data-quality scoring.

---

## Prediction Module

The Prediction Module estimates future system states.

Capabilities include:

- Temperature prediction.
- Pressure prediction.
- Flow prediction.
- Phase-state prediction.
- Vapor-fraction prediction.
- Thermal-gradient prediction.
- Transfer-state prediction.
- System-response prediction.
- Uncertainty estimation.
- Prediction-horizon management.

The Prediction Module allows ForwardState to evaluate where the system is going rather than simply responding to where it is now.

---

## Digital Twin Module

The Digital Twin Module maintains a computational representation of the physical system.

Capabilities include:

- Live state synchronization.
- Physical parameter modeling.
- Thermodynamic modeling.
- Flow modeling.
- Thermal modeling.
- Pressure modeling.
- Phase modeling.
- Model calibration.
- Model divergence detection.
- Simulation replay.
- Historical state reconstruction.

The digital twin can operate in real time or independently for development and testing.

---

## Model Predictive Control Module

The Model Predictive Control Module determines control actions using predicted future states.

Capabilities include:

- Predictive control.
- Constraint management.
- Multi-variable control.
- Control-horizon management.
- Actuator optimization.
- Thermal control.
- Pressure control.
- Flow control.
- Conditioning control.
- Transfer-rate control.
- Safe-state transitions.

The controller should operate within deterministic system and safety constraints.

---

## Control Coordination Module

The Control Coordination Module converts high-level control decisions into coordinated actions.

Capabilities include:

- Valve coordination.
- Pump coordination.
- Thermal-system coordination.
- Transfer-path selection.
- Conditioning sequence control.
- Multi-actuator coordination.
- Command sequencing.
- Command validation.
- Actuator-state verification.
- Controlled startup and shutdown.

---

## Phase-State Module

The Phase-State Module evaluates the physical state of the propellant and transfer system.

Capabilities include:

- Liquid-state estimation.
- Vapor-state estimation.
- Two-phase-flow detection.
- Phase-transition detection.
- Vapor-fraction estimation.
- Flash-boil detection.
- Phase-boundary prediction.
- Phase-stability monitoring.

The module provides information required for controlled cryogenic transfer.

---

## Thermal Intelligence Module

The Thermal Intelligence Module evaluates system thermal behavior.

Capabilities include:

- Thermal-state estimation.
- Thermal-gradient detection.
- Thermal-response prediction.
- Heat-leak estimation.
- Chill-down monitoring.
- Thermal stabilization detection.
- Thermal excursion detection.
- Thermal-state forecasting.

---

## Pressure Intelligence Module

The Pressure Intelligence Module evaluates current and predicted pressure behavior.

Capabilities include:

- Pressure-state estimation.
- Pressure-rate monitoring.
- Pressure prediction.
- Differential-pressure monitoring.
- Pressure instability detection.
- Pressure spike prediction.
- Pressure decay detection.
- Pressure-envelope monitoring.

---

## Flow Intelligence Module

The Flow Intelligence Module evaluates movement through the physical system.

Capabilities include:

- Flow-state estimation.
- Flow prediction.
- Flow-rate optimization.
- Flow instability detection.
- Restriction detection.
- Pump performance monitoring.
- Valve performance monitoring.
- Transfer-rate optimization.

---

## Anomaly Detection Module

The Anomaly Detection Module identifies conditions that differ from expected system behavior.

Capabilities include:

- Sensor anomalies.
- Thermal anomalies.
- Pressure anomalies.
- Flow anomalies.
- Phase anomalies.
- Pump anomalies.
- Valve anomalies.
- Communication anomalies.
- Model divergence.
- Unexpected system responses.

The module can compare observed behavior against both historical data and predicted behavior.

---

## Fault Management Module

The Fault Management Module coordinates system response to detected failures.

Capabilities include:

- Fault classification.
- Fault isolation.
- Fault prioritization.
- Recovery sequencing.
- Redundant-system selection.
- Degraded-operation management.
- Safe-state requests.
- Recovery verification.
- Fault history.

Fault management operates below higher-level optimization and mission-planning functions.

---

## Safety Boundary Module

The Safety Boundary Module establishes deterministic limits around ForwardState operations.

Capabilities include:

- Temperature limits.
- Pressure limits.
- Flow limits.
- Actuator limits.
- Rate-of-change limits.
- Operating-envelope enforcement.
- Command validation.
- Interlock interfaces.
- Emergency-state requests.
- Control-output rejection.

Predictive, adaptive, and AI-driven systems must remain subordinate to defined safety constraints.

---

## Telemetry Module

The Telemetry Module manages system data.

Capabilities include:

- Real-time telemetry.
- Event logging.
- State logging.
- Control-decision logging.
- Prediction logging.
- Fault logging.
- Command logging.
- Historical data storage.
- Data replay.
- External telemetry interfaces.

---

## PhaseLock Integration Module

The PhaseLock Integration Module provides the primary physical-system interface.

ForwardState receives information from PhaseLock and provides validated predictive-control outputs.

The integration can include:

- Temperature telemetry.
- Pressure telemetry.
- Flow telemetry.
- Phase-state data.
- Pump states.
- Valve states.
- Conditioning state.
- Safety state.
- Fault state.
- Control requests.
- Transfer-state information.

PhaseLock repository:

[PhaseLock](https://gitlab.com/Roxanne_Ardary/phaselock)

The intended relationship is:

PhaseLock → Sensors → ForwardState → Prediction → Control Decision → PhaseLock

---

## Configuration Module

The Configuration Module allows ForwardState to support different deployments.

Configuration may define:

- Propellant.
- Tank geometry.
- Transfer architecture.
- Sensor configuration.
- Actuator configuration.
- System constraints.
- Control parameters.
- Prediction models.
- Safety boundaries.
- Telemetry interfaces.
- Plugin configuration.

Configuration should remain separate from executable control logic whenever practical.

---

## Event and Decision Module

The Event and Decision Module records significant system events and control decisions.

Capabilities include:

- Event classification.
- Decision recording.
- Prediction snapshots.
- Control-action recording.
- Operator-action recording.
- Fault-event recording.
- State-transition logging.
- Decision replay.

This creates an auditable operational history.

---

# Optional Plugin Modules

ForwardState supports an optional plugin architecture for advanced capabilities.

Plugins should use documented interfaces and must not bypass Core Safety or deterministic control boundaries.

---

## AI Prediction Plugin

Extends the standard prediction engine with machine-learning models.

Capabilities include:

- Learned system models.
- Time-series prediction.
- Nonlinear prediction.
- Pattern recognition.
- Transfer-performance prediction.
- Model comparison.

AI predictions should remain bounded by validated physical models and safety constraints.

---

## AI Anomaly Detection Plugin

Provides machine-learning-assisted anomaly detection.

Capabilities include:

- Behavioral anomaly detection.
- Multivariate anomaly detection.
- Unknown-pattern identification.
- Sensor-failure classification.
- Predictive failure indicators.
- Historical-pattern comparison.

---

## Adaptive Learning Plugin

Allows models to improve from validated operational data.

Capabilities include:

- Parameter adaptation.
- System identification.
- Model refinement.
- Transfer-to-transfer learning.
- Performance optimization.
- Prediction-error analysis.

Adaptive learning must not automatically alter safety boundaries.

---

## Reinforcement Learning Plugin

Provides optional reinforcement-learning experimentation for control optimization.

Capabilities include:

- Policy evaluation.
- Simulation-based training.
- Control-policy comparison.
- Reward modeling.
- Scenario optimization.

Reinforcement-learning policies should initially operate within simulation, digital-twin, or supervised environments before consideration for physical deployment.

---

## Advanced Thermodynamics Plugin

Provides higher-fidelity thermodynamic calculations.

Capabilities include:

- Equation-of-state modeling.
- Enthalpy calculations.
- Density calculations.
- Phase-equilibrium calculations.
- Vapor-liquid equilibrium.
- Heat-transfer calculations.
- Propellant-specific thermodynamic models.

---

## Propellant Plugin

Provides specialized models for individual propellants.

Potential configurations include:

- LOX.
- LH2.
- LCH4.
- Other cryogenic propellants.

A propellant plugin can provide:

- Thermodynamic properties.
- Phase behavior.
- Operating envelopes.
- Model parameters.
- Sensor requirements.
- Control constraints.

---

## Tank Model Plugin

Provides specialized tank models.

Capabilities include:

- Tank geometry.
- Thermal behavior.
- Pressure behavior.
- Stratification.
- Fluid distribution.
- Tank-state estimation.
- Tank-specific simulation.

---

## Slosh Prediction Plugin

Provides predictive modeling of fluid movement in microgravity.

Capabilities include:

- Slosh estimation.
- Slosh prediction.
- Attitude correlation.
- Transfer-induced disturbances.
- Tank-state correlation.
- Slosh-aware control.

---

## Multi-Tank Coordination Plugin

Coordinates multiple connected tanks.

Capabilities include:

- Tank allocation.
- Flow balancing.
- Tank prioritization.
- Transfer routing.
- Inventory balancing.
- Tank-state synchronization.

---

## Multi-Vehicle Coordination Plugin

Extends ForwardState to multiple spacecraft.

Capabilities include:

- Vehicle-state tracking.
- Transfer coordination.
- Resource allocation.
- Vehicle prioritization.
- Concurrent transfer management.
- Fleet-level optimization.

---

## Depot Network Plugin

Provides network-level orbital propellant management.

Capabilities include:

- Depot discovery.
- Depot inventory.
- Propellant availability.
- Transfer scheduling.
- Depot selection.
- Network optimization.
- Resource forecasting.

---

## Mission Planning Plugin

Provides planning and sequencing capabilities.

Capabilities include:

- Transfer planning.
- Conditioning planning.
- Mission sequencing.
- Resource planning.
- Timing optimization.
- Abort planning.
- Recovery planning.

---

## Autonomous Scheduling Plugin

Optimizes multiple operations over time.

Capabilities include:

- Refueling-window optimization.
- Vehicle scheduling.
- Depot scheduling.
- Conditioning-time optimization.
- Resource allocation.
- Mission-priority management.

---

## Predictive Maintenance Plugin

Provides component health forecasting.

Capabilities include:

- Pump health.
- Valve health.
- Sensor degradation.
- Controller health.
- Communication health.
- Component lifetime estimation.
- Maintenance forecasting.

---

## Hardware-in-the-Loop Plugin

Provides interfaces for physical test systems.

Capabilities include:

- Simulated sensors.
- Simulated actuators.
- Real controller integration.
- Failure injection.
- Hardware testing.
- Automated test scenarios.
- Real-time simulation.

---

## Monte Carlo Testing Plugin

Provides large-scale uncertainty and failure analysis.

Capabilities include:

- Parameter variation.
- Sensor failures.
- Actuator failures.
- Thermal excursions.
- Pressure excursions.
- Flow disturbances.
- Communication failures.
- Model uncertainty.
- Safety-margin analysis.

---

## Mission Simulation Plugin

Provides complete mission-level simulation.

Capabilities include:

- Vehicle simulation.
- Depot simulation.
- Transfer simulation.
- Environmental modeling.
- Mission timeline simulation.
- Failure scenarios.
- Recovery scenarios.

---

## Visualization Plugin

Provides advanced visualization of ForwardState operations.

Capabilities include:

- Live system state.
- Prediction horizons.
- Digital-twin state.
- Thermal state.
- Pressure state.
- Flow state.
- Phase state.
- Control outputs.
- Fault states.
- Historical replay.

---

## Operator Interface Plugin

Provides human-in-the-loop operations.

Capabilities include:

- System monitoring.
- Control authorization.
- Alarm management.
- Transfer approval.
- Manual hold.
- Recovery authorization.
- Mission-state visualization.
- Event review.

Operator commands remain subject to Core Safety boundaries.

---

## Explainability Plugin

Provides explanations of predictive and control decisions.

Capabilities include:

- Prediction reasoning.
- Control-action explanation.
- Anomaly explanation.
- Model comparison.
- Confidence reporting.
- Decision history.

---

## Audit Plugin

Provides detailed operational traceability.

Capabilities include:

- Decision logs.
- Prediction logs.
- Control logs.
- Operator actions.
- Configuration history.
- Model-version history.
- Fault history.
- Transfer history.

---

## Cloud Analytics Plugin

Provides optional ground-based analytics.

Capabilities include:

- Fleet analytics.
- Mission analytics.
- Historical comparison.
- Transfer optimization.
- Performance analysis.
- Model training datasets.
- Cross-mission trend analysis.

Cloud services are optional and are not required for local operation.

---

## External API Plugin

Provides interfaces for external software.

Potential interfaces include:

- REST.
- GraphQL.
- Message-based interfaces.
- Telemetry APIs.
- Mission-control APIs.
- Depot-management APIs.

---

# Control Hierarchy

ForwardState separates deterministic safety from prediction, optimization, and autonomy.

The preferred hierarchy is:

1. Physical hardware constraints
2. Independent safety controls
3. Core safety boundaries
4. Core control modules
5. Predictive control
6. Optimization
7. AI and adaptive systems
8. Mission planning
9. Operator and external commands

No higher-level system should be capable of bypassing lower-level safety constraints.

---

# Operating States

ForwardState supports explicit system states.

### Initialization

Load configuration, verify dependencies, initialize modules, and establish communications.

### Self-Test

Verify sensors, models, communications, control interfaces, and system health.

### Monitoring

Observe the physical system without issuing active control commands.

### Estimation

Maintain the current system state and uncertainty estimates.

### Prediction

Generate future-state predictions.

### Control Ready

Verify that predictions, models, actuators, and safety boundaries are valid for control.

### Predictive Control

Generate and validate control actions.

### Coordinated Transfer

Coordinate control actions with PhaseLock during propellant transfer.

### Hold

Temporarily suspend active transfer commands while continuing system monitoring and prediction.

### Fault Response

Evaluate detected anomalies and determine an appropriate response.

### Recovery

Attempt to restore normal operation within defined safety boundaries.

### Safe State

Stop or constrain control activity and request the appropriate physical safe state.

### Shutdown

Persist state, logs, decisions, and operational data before terminating active control.

---

# Prediction Pipeline

The primary ForwardState workflow is:

1. Receive telemetry.
2. Validate incoming data.
3. Synchronize timestamps.
4. Fuse sensor information.
5. Estimate the current state.
6. Update the digital twin.
7. Generate future-state predictions.
8. Evaluate uncertainty.
9. Identify potential instability.
10. Generate candidate control actions.
11. Apply safety constraints.
12. Select the valid control action.
13. Send the command to PhaseLock.
14. Observe the resulting system response.
15. Update the state estimate.
16. Record the prediction and decision.
17. Repeat.

This creates a continuous closed-loop predictive-control process.

---

# PhaseLock Integration

ForwardState is designed as the software intelligence layer for PhaseLock.

PhaseLock provides:

- Cryogenic conditioning.
- Pumps.
- Valves.
- Sensors.
- Transfer paths.
- Vapor management.
- Thermal management.
- Physical safety mechanisms.

ForwardState provides:

- State estimation.
- Prediction.
- Digital-twin modeling.
- Model predictive control.
- Anomaly detection.
- Optimization.
- Coordination.
- Operational intelligence.

Together they form a layered system:

**PhaseLock**

Physical cryogenic conditioning and transfer

↓

**ForwardState**

Prediction, estimation, control, and intelligence

↓

**PhaseLock**

Validated physical actuation

---

# Simulation and Verification

ForwardState should be validated progressively.

## Software Simulation

Test:

- State estimation.
- Prediction.
- Control algorithms.
- Failure conditions.
- Sensor behavior.
- Actuator behavior.

## Digital Twin

Compare predicted behavior against modeled physical behavior.

## Hardware-in-the-Loop

Run ForwardState against real controllers and simulated physical systems.

## Ground Hardware

Validate integration with actual sensors, valves, pumps, and control hardware.

## Integrated System

Validate ForwardState with PhaseLock and associated spacecraft or depot interfaces.

## Flight Qualification

Any flight implementation requires appropriate mission-specific engineering, verification, qualification, and safety processes.

---

# Fault Handling

ForwardState should distinguish between:

- Sensor failure.
- Actuator failure.
- Communication failure.
- Model failure.
- Prediction uncertainty.
- Physical anomaly.
- Control failure.
- External-system failure.

Fault handling should provide:

- Detection.
- Classification.
- Isolation.
- Prioritization.
- Response.
- Recovery.
- Verification.
- Logging.

---

# Data Architecture

ForwardState should maintain structured records for:

- Sensor observations.
- Estimated states.
- Prediction states.
- Model versions.
- Control actions.
- Safety decisions.
- Fault events.
- Operator actions.
- Configuration changes.
- Mission events.

All critical events should use synchronized timestamps.

---

# Local-First Operation

ForwardState is designed to operate without mandatory cloud connectivity.

Core operation should remain available through local computing resources.

Cloud services may be added through optional plugins for:

- Analytics.
- Fleet management.
- Model training.
- Long-term storage.
- Cross-mission analysis.

Loss of cloud connectivity must not prevent required local safety and control functions.

---

# Interoperability

ForwardState should avoid vendor lock-in.

The architecture should support:

- Multiple sensor manufacturers.
- Multiple actuator manufacturers.
- Multiple flight computers.
- Multiple RTOS platforms.
- Multiple simulation platforms.
- Multiple telemetry systems.
- Multiple thermodynamic models.
- Multiple control frameworks.

---

# Technology Stack

The implementation may use:

- **Rust** for safety-oriented and performance-critical components.
- **Python** for simulation, testing, orchestration, and engineering tools.
- **Julia** for advanced scientific and mathematical modeling where appropriate.
- **CasADi** for optimization and model predictive control development.
- **acados** for high-performance predictive-control implementations.
- **Modelica** for physical-system and thermodynamic modeling.
- **Zephyr RTOS** for supported embedded deployments.
- **RTEMS or real-time Linux** for appropriate real-time computing environments.
- **ROS 2 and DDS** where their communication architecture is appropriate.
- **ONNX Runtime** for supported machine-learning inference.
- **TimescaleDB or InfluxDB** for telemetry storage and analysis.
- **Plotly Dash or Streamlit** for engineering and operations interfaces.

Technology choices remain modular and may be replaced when another implementation provides better determinism, reliability, portability, or mission suitability.

---

# Plugin Architecture

Plugins should:

- Use documented APIs.
- Declare dependencies.
- Declare supported configurations.
- Provide configuration schemas.
- Provide tests.
- Provide documentation.
- Define failure behavior.
- Remain independently disableable.
- Respect Core Safety boundaries.
- Avoid direct modification of safety-critical logic.

A plugin failure must not compromise the Core Safety Module.

---

# Development Principles

ForwardState development follows these principles:

- Modular architecture.
- Local-first operation.
- Deterministic safety.
- Predictive control.
- Hardware independence.
- Vendor independence.
- Human oversight.
- Reproducible testing.
- Digital-twin validation.
- Hardware-in-the-loop validation.
- Fault tolerance.
- Explicit operating states.
- Auditable decisions.
- Separation of safety and optimization.
- Replaceable components.
- Documented interfaces.

---

# Testing Requirements

New functionality should include appropriate validation.

Testing may include:

- Unit testing.
- Integration testing.
- Simulation testing.
- Digital-twin testing.
- Hardware-in-the-loop testing.
- Fault-injection testing.
- Regression testing.
- Monte Carlo testing.
- Prediction accuracy testing.
- Control stability testing.
- Sensor-fusion testing.
- Model validation.

Safety-critical changes require additional verification appropriate to the affected subsystem.

---

# Documentation

Changes should document:

- Architecture.
- Interfaces.
- Models.
- Configuration.
- Operating states.
- Control behavior.
- Safety behavior.
- Failure behavior.
- Plugin requirements.
- Testing.
- Integration requirements.

---

# Relationship to [PhaseLock](https://gitlab.com/Roxanne_Ardary/phaselock)  

ForwardState is designed to operate with [PhaseLock](https://gitlab.com/Roxanne_Ardary/phaselock).

**PhaseLock** provides the physical Cryogenic Conditioning Loop.

**ForwardState** provides the predictive software stack.

The two systems create a closed-loop architecture:

**PhaseLock → Telemetry → ForwardState → Prediction → Control Decision → PhaseLock**

PhaseLock handles the physical system.

ForwardState determines where the system is going and helps determine how to keep it within its desired operating state.

---

**ForwardState**

*Holding Balance Before It Drifts.*

---

## Specification Branding License (SBL)
### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/forwardstate/](https://roxanneardary.com/forwardstate/)

---

## License & Notice Requirements

ForwardState is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- ForwardState specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

---

PhaseLock + ForwardState: The foundation for reusable space.
Predict. Align. Transfer.
