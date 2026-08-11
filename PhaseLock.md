# PhaseLock + ForwardState

*PhaseLock – The Key to Reusable Space.*  
*ForwardState – Holding Balance Before It Drifts.*  [ForwardState Codeberg Repository](https://codeberg.org/RoxanneA/ForwardState)

PhaseLock is a modular Cryogenic Conditioning Loop (CCL) specification for controlled in-space cryogenic propellant conditioning, transfer, and refueling. The system is designed to manage temperature, pressure, phase behavior, circulation, vapor, and flow throughout the transfer process.

PhaseLock is designed to work with **ForwardState**, its predictive software counterpart. PhaseLock provides the physical conditioning and control interface, while ForwardState provides predictive state estimation, digital-twin modeling, model predictive control, anomaly detection, optimization, and higher-level autonomy.

The architecture prioritizes modularity, redundancy, simulation, local operation, interoperability, and the ability to support different spacecraft, tanks, transfer interfaces, propellants, sensors, pumps, valves, and control platforms without redesigning the entire system.

---

## Project Goals

PhaseLock is designed to:

- Condition cryogenic propellant before transfer.
- Maintain controlled thermal and pressure conditions.
- Minimize unwanted phase changes during transfer.
- Manage vapor generation and recondensation.
- Reduce thermal shock during chill-down.
- Maintain stable circulation through the conditioning loop.
- Provide precise sensor and actuator interfaces.
- Support autonomous and supervised refueling operations.
- Integrate with ForwardState for predictive control.
- Support multiple spacecraft and depot configurations.
- Provide redundant and fault-tolerant control paths.
- Enable hardware-in-the-loop and digital-twin validation.
- Support modular replacement and local manufacturing of components.
- Avoid dependence on a single vendor, spacecraft, or propulsion architecture.

---

# System Architecture

PhaseLock uses a layered modular architecture.

### Core System

The Core System provides the minimum infrastructure required for a functional Cryogenic Conditioning Loop.

### Core Modules

Core modules provide the essential physical, sensing, control, safety, and communication capabilities of PhaseLock.

### Optional Plugin Modules

Plugin modules extend PhaseLock for specialized propellants, hardware configurations, missions, analytics, autonomy, visualization, and external systems.

### External Systems

PhaseLock can integrate with:

- ForwardState
- Spacecraft flight computers
- Orbital depots
- Mission control systems
- Digital twins
- Simulation environments
- Ground support systems
- External telemetry systems

---

# Core Modules

## Core Loop Module

The Core Loop Module manages circulation of cryogenic propellant through the conditioning system.

Capabilities include:

- Closed-loop circulation.
- Flow routing.
- Recirculation control.
- Transfer-line conditioning.
- Loop pressure management.
- Flow stabilization.
- Pump coordination.
- Valve sequencing.
- Conditioning-loop isolation.
- Return-path management.
- Transfer-path management.
- Loop state monitoring.

The module provides the physical foundation for all other PhaseLock functions.

---

## Thermal Conditioning Module

The Thermal Conditioning Module controls the thermal state of the propellant and associated transfer hardware.

Capabilities include:

- Controlled chill-down.
- Thermal stabilization.
- Temperature monitoring.
- Thermal-gradient detection.
- Thermal-gradient management.
- Transfer-line conditioning.
- Component temperature tracking.
- Thermal shock mitigation.
- Heat-leak monitoring.
- Propellant temperature control.
- Pre-transfer thermal conditioning.
- Continuous thermal conditioning during transfer.

The module is designed to prevent uncontrolled thermal transitions from destabilizing the transfer process.

---

## Phase Management Module

The Phase Management Module monitors and manages liquid, vapor, and transitional states within the conditioning system.

Capabilities include:

- Phase-state estimation.
- Vapor detection.
- Vapor fraction estimation.
- Phase-boundary tracking.
- Flash-boil detection.
- Two-phase-flow detection.
- Phase-transition monitoring.
- Liquid-state stabilization.
- Vapor routing.
- Recondensation coordination.
- Phase-state alarms.
- Transfer-state qualification.

The module provides the foundation for controlled single-phase transfer when mission and propellant conditions permit it.

---

## Pressure Management Module

The Pressure Management Module maintains pressure within defined operating envelopes.

Capabilities include:

- Pressure monitoring.
- Differential-pressure monitoring.
- Pressure-rate monitoring.
- Pressure prediction interfaces.
- Pressure stabilization.
- Pressure relief coordination.
- Pressure spike detection.
- Pressure decay detection.
- Pressure balancing.
- Tank-to-loop pressure coordination.
- Transfer pressure control.
- Emergency pressure isolation.

Pressure limits are configurable for the specific hardware and propellant configuration.

---

## Flow Management Module

The Flow Management Module controls movement of propellant throughout PhaseLock.

Capabilities include:

- Flow-rate measurement.
- Flow-rate control.
- Pump control.
- Valve control.
- Flow balancing.
- Flow restriction detection.
- Flow instability detection.
- Transfer-rate management.
- Recirculation control.
- Transfer-path selection.
- Flow interruption detection.
- Controlled startup and shutdown.

---

## Vapor Management Module

The Vapor Management Module manages vapor created during conditioning and transfer.

Capabilities include:

- Vapor detection.
- Vapor accumulation monitoring.
- Vapor routing.
- Vapor separation.
- Recondensation control.
- Vapor return paths.
- Pressure stabilization.
- Mass-balance tracking.
- Boil-off monitoring.
- Vapor recovery.
- Vapor isolation.
- Emergency vent-management interfaces.

The module is designed to reduce unnecessary propellant loss while maintaining safe pressure and phase conditions.

---

## Chill-Down Module

The Chill-Down Module performs controlled thermal preparation of the transfer system.

Capabilities include:

- Staged chill-down.
- Controlled flow ramping.
- Thermal gradient monitoring.
- Component temperature qualification.
- Transfer-line conditioning.
- Pump conditioning.
- Valve conditioning.
- Chill-down completion detection.
- Thermal stabilization verification.
- Abort and recovery sequences.

The module prevents rapid thermal transitions from compromising transfer hardware or propellant stability.

---

## Sensor Module

The Sensor Module provides standardized interfaces for PhaseLock instrumentation.

Supported sensor categories include:

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
- Thermal state.
- Leak detection.

Capabilities include:

- Sensor registration.
- Sensor calibration.
- Sensor validation.
- Sensor redundancy.
- Sensor fusion.
- Sensor-health monitoring.
- Sensor drift detection.
- Outlier rejection.
- Timestamp synchronization.
- Sensor failure identification.

---

## Actuator Module

The Actuator Module provides standardized interfaces for physical control devices.

Supported actuators include:

- Cryogenic pumps.
- Valves.
- Microvalves.
- Flow-control devices.
- Isolation devices.
- Thermal-control devices.
- Recondensation equipment.
- Pressure-control equipment.

Capabilities include:

- Command validation.
- Position verification.
- Actuator health monitoring.
- Redundant actuator control.
- Controlled startup.
- Controlled shutdown.
- Fail-safe positioning.
- Emergency isolation.
- Command-rate limiting.

---

## Safety Module

The Safety Module provides independent safety monitoring and protective actions.

Capabilities include:

- Operating-envelope enforcement.
- Pressure-limit monitoring.
- Temperature-limit monitoring.
- Flow-limit monitoring.
- Leak detection.
- Sensor-failure detection.
- Actuator-failure detection.
- Emergency isolation.
- Transfer abort.
- Safe-state control.
- Redundant safety paths.
- Interlock management.
- Fault containment.
- Recovery-state management.

Safety functions should remain independently verifiable from higher-level optimization and autonomy systems.

---

## Redundancy and Fault-Tolerance Module

This module prevents individual component failures from unnecessarily terminating a mission operation.

Capabilities include:

- Redundant sensor paths.
- Redundant actuator paths.
- Redundant controllers.
- Automatic failover.
- Sensor voting.
- Fault isolation.
- Degraded-operation modes.
- Component bypass.
- Alternate flow paths.
- Recovery sequencing.
- Fault-state persistence.
- Single-point-failure analysis.

---

## Telemetry Module

The Telemetry Module provides standardized communication between PhaseLock components and external systems.

Capabilities include:

- Real-time telemetry.
- Sensor data publishing.
- Actuator-state publishing.
- System-state reporting.
- Event logging.
- Fault reporting.
- Command acknowledgement.
- Time synchronization.
- Data buffering.
- Telemetry prioritization.
- Local telemetry storage.
- External telemetry interfaces.

---

## ForwardState Integration Module

The ForwardState Integration Module connects PhaseLock with the predictive software layer.

ForwardState can provide:

- Predictive state estimation.
- Digital-twin state.
- Model predictive control.
- Future-state predictions.
- Thermal predictions.
- Pressure predictions.
- Phase predictions.
- Anomaly detection.
- Optimization recommendations.
- Refueling sequence planning.
- Fault prediction.

PhaseLock remains responsible for validating and executing physical control actions within its configured safety boundaries.

ForwardState repository:

[ForwardState](https://codeberg.org/RoxanneA/ForwardState)

---

## Configuration Module

The Configuration Module allows PhaseLock to support different hardware and mission configurations.

Configuration parameters may include:

- Propellant type.
- Tank geometry.
- Transfer-line geometry.
- Pump characteristics.
- Valve characteristics.
- Sensor types.
- Sensor ranges.
- Actuator limits.
- Pressure limits.
- Temperature limits.
- Flow limits.
- Conditioning targets.
- Safety thresholds.
- Redundancy configuration.
- Telemetry configuration.

Configuration should be separated from core control logic wherever practical.

---

## Diagnostics Module

The Diagnostics Module continuously evaluates PhaseLock system health.

Capabilities include:

- Component health monitoring.
- Sensor diagnostics.
- Pump diagnostics.
- Valve diagnostics.
- Thermal diagnostics.
- Pressure diagnostics.
- Flow diagnostics.
- Leak diagnostics.
- Communication diagnostics.
- Fault classification.
- Fault history.
- Maintenance indicators.

---

# Optional Plugin Modules

PhaseLock supports an optional plugin architecture for capabilities that are not required by every deployment.

Plugins should use documented interfaces and should not modify the safety-critical Core System directly.

---

## Propellant Plugin

Provides propellant-specific models and operating parameters.

Potential support includes:

- LOX.
- LH2.
- LCH4.
- Other cryogenic propellants.
- Mixed or specialized propellant configurations.

Each propellant plugin can define:

- Thermodynamic properties.
- Operating envelopes.
- Phase behavior.
- Conditioning requirements.
- Sensor requirements.
- Safety constraints.
- Control parameters.

---

## Tank Geometry Plugin

Provides geometry-specific models for:

- Spherical tanks.
- Cylindrical tanks.
- Composite tanks.
- Depot tanks.
- Vehicle tanks.
- Transfer vessels.
- Specialized cryogenic storage systems.

The plugin can provide geometry data for thermal, pressure, flow, and phase models.

---

## Slosh Dynamics Plugin

Provides advanced modeling of fluid movement in microgravity.

Capabilities include:

- Slosh estimation.
- Slosh prediction.
- Tank attitude correlation.
- Transfer-induced disturbances.
- Propellant movement modeling.
- Attitude-control integration.
- Slosh-aware transfer optimization.

---

## Thermal Stratification Plugin

Provides advanced internal tank thermal modeling.

Capabilities include:

- Thermal-layer estimation.
- Temperature-gradient mapping.
- Stratification prediction.
- Heat-transfer modeling.
- Phase-boundary prediction.
- Stratification-aware transfer planning.

---

## Adaptive Control Plugin

Extends the standard control system with adaptive optimization.

Capabilities include:

- Adaptive MPC parameters.
- System identification.
- Transfer-to-transfer learning.
- Model parameter updates.
- Performance optimization.
- Efficiency tracking.

Adaptive algorithms must remain subject to defined safety constraints.

---

## AI Anomaly Detection Plugin

Provides machine-learning-assisted anomaly detection.

Capabilities include:

- Sensor anomaly detection.
- Pressure anomaly detection.
- Temperature anomaly detection.
- Flow anomaly detection.
- Pump anomaly detection.
- Valve anomaly detection.
- Leak-pattern detection.
- Thermal anomaly detection.
- Predictive failure indicators.

AI-generated recommendations should remain subordinate to deterministic safety controls.

---

## Predictive Maintenance Plugin

Provides component health forecasting.

Capabilities include:

- Pump wear estimation.
- Valve-cycle analysis.
- Sensor degradation monitoring.
- Component lifetime estimation.
- Maintenance forecasting.
- Replacement recommendations.
- Reliability analysis.

---

## Digital Twin Plugin

Provides advanced simulation synchronization.

Capabilities include:

- Live digital-twin synchronization.
- Parameter calibration.
- Model comparison.
- State reconstruction.
- Simulation-versus-reality analysis.
- Model divergence detection.
- Digital-twin replay.

---

## Hardware-in-the-Loop Plugin

Provides interfaces for laboratory and hardware-in-the-loop testing.

Capabilities include:

- Sensor simulation.
- Actuator simulation.
- Pump simulation.
- Valve simulation.
- Thermal simulation.
- Pressure simulation.
- Failure injection.
- Automated test scenarios.
- Hardware controller integration.

---

## Monte Carlo Testing Plugin

Provides large-scale scenario testing.

Capabilities include:

- Randomized parameter variation.
- Sensor-failure scenarios.
- Pump-failure scenarios.
- Valve-failure scenarios.
- Thermal excursions.
- Pressure excursions.
- Flow disruptions.
- Communication failures.
- Model uncertainty analysis.
- Safety-margin analysis.

---

## Mission Planning Plugin

Provides automated planning of conditioning and transfer operations.

Capabilities include:

- Transfer sequence generation.
- Conditioning sequence planning.
- Timing optimization.
- Safety-margin selection.
- Resource planning.
- Abort-condition planning.
- Recovery planning.

---

## Autonomous Scheduling Plugin

Provides scheduling across multiple operations.

Capabilities include:

- Refueling-window optimization.
- Depot scheduling.
- Vehicle scheduling.
- Conditioning-time optimization.
- Resource allocation.
- Multi-vehicle coordination.
- Multi-depot scheduling.

---

## Multi-Vehicle Plugin

Enables coordination between multiple spacecraft.

Capabilities include:

- Multiple transfer sessions.
- Tank allocation.
- Flow allocation.
- Resource balancing.
- Transfer prioritization.
- Vehicle-state coordination.
- Concurrent operation management.

---

## Multi-Depot Plugin

Extends PhaseLock for orbital infrastructure networks.

Capabilities include:

- Depot discovery.
- Depot-state synchronization.
- Propellant availability tracking.
- Cross-depot planning.
- Transfer-path optimization.
- Network resource management.

---

## Autonomous Docking Integration Plugin

Provides interfaces between docking systems and refueling operations.

Capabilities include:

- Docking-state monitoring.
- Transfer-interface verification.
- Alignment-state monitoring.
- Mechanical connection verification.
- Transfer authorization.
- Docking disturbance awareness.
- Automatic transfer hold during unsafe conditions.

---

## Mission Control Plugin

Provides interfaces for human operators.

Capabilities include:

- Remote monitoring.
- Command interfaces.
- Transfer authorization.
- Safety-state visualization.
- Alarm management.
- Mission event logging.
- Manual override.
- Operator acknowledgement.

Human commands remain subject to PhaseLock safety interlocks.

---

## Visualization Plugin

Provides advanced system visualization.

Capabilities include:

- Live loop visualization.
- Thermal visualization.
- Pressure visualization.
- Flow visualization.
- Phase-state visualization.
- Tank-state visualization.
- Transfer progress.
- System health.
- Historical replay.

---

## Augmented Reality Plugin

Provides optional spatial visualization for engineering and mission operations.

Capabilities include:

- System-state overlays.
- Tank visualization.
- Flow visualization.
- Component identification.
- Fault visualization.
- Maintenance guidance.
- Transfer-state visualization.

---

## Cloud Analytics Plugin

Provides optional ground-side analytics.

Capabilities include:

- Historical telemetry analysis.
- Fleet analytics.
- Transfer comparison.
- Predictive modeling.
- Mission trend analysis.
- Performance benchmarking.
- Cross-mission learning.

Cloud functionality is optional and is not required for local PhaseLock operation.

---

## External API Plugin

Provides standardized interfaces for external software.

Potential interfaces include:

- REST APIs.
- GraphQL.
- Message-based APIs.
- Telemetry APIs.
- Mission-control interfaces.
- Depot-management interfaces.

---

# Control Hierarchy

PhaseLock separates deterministic safety from optimization and autonomy.

The preferred hierarchy is:

1. **Physical hardware limits**
2. **Independent safety controls**
3. **Core control modules**
4. **ForwardState predictive control**
5. **Optimization systems**
6. **AI and machine-learning recommendations**
7. **Mission scheduling**
8. **Operator and external commands**

Higher-level systems must never bypass lower-level safety constraints.

---

# Operating States

PhaseLock supports defined operating states.

### Standby

System powered and monitoring but not conditioning or transferring propellant.

### Self-Test

Sensors, actuators, communications, and safety systems are verified.

### Conditioning

The system establishes the required thermal, pressure, and phase conditions.

### Chill-Down

Transfer hardware and associated components are progressively brought toward operating conditions.

### Stabilization

The system verifies that thermal, pressure, flow, and phase conditions remain within configured limits.

### Transfer Ready

All transfer authorization conditions are satisfied.

### Transfer

Controlled propellant movement occurs between the source and receiving system.

### Hold

Transfer is temporarily suspended while the system maintains safe conditions.

### Recovery

The system responds to a recoverable anomaly and attempts to restore stable operation.

### Safe State

The system isolates affected components and places the system into a predefined safe configuration.

### Shutdown

The system completes the transfer, secures the loop, and records final operational data.

---

# Safety Architecture

Safety is implemented as a layered system.

PhaseLock should provide:

- Independent safety limits.
- Hardware-level isolation where appropriate.
- Redundant critical sensing.
- Deterministic interlocks.
- Fail-safe actuator states.
- Emergency transfer termination.
- Fault containment.
- Controlled recovery.
- Explicit authorization states.
- Independent verification of safety-critical commands.

AI and adaptive systems must not be permitted to directly override deterministic safety limits.

---

# Simulation and Verification

PhaseLock should be validated progressively before deployment.

### Software Simulation

Test:

- Thermal behavior.
- Pressure behavior.
- Flow behavior.
- Phase transitions.
- Control logic.
- Fault conditions.

### Digital Twin

Compare predicted system behavior with simulated and experimental behavior.

### Hardware-in-the-Loop

Connect actual controllers and interfaces to simulated cryogenic-system behavior.

### Ground Hardware Testing

Validate sensors, valves, pumps, thermal systems, communications, and safety functions under controlled conditions.

### Integrated Testing

Validate PhaseLock with ForwardState and associated spacecraft or depot interfaces.

### Flight Qualification

Any flight implementation must undergo appropriate engineering, verification, qualification, and mission-specific safety processes.

---

# Data and Telemetry

PhaseLock should record sufficient information to reconstruct system behavior.

Telemetry may include:

- Temperature.
- Pressure.
- Differential pressure.
- Flow.
- Mass flow.
- Valve positions.
- Pump states.
- Tank states.
- Phase estimates.
- Conditioning state.
- Safety state.
- Fault state.
- ForwardState predictions.
- Control decisions.
- Operator commands.
- Transfer events.
- System transitions.

Data should use synchronized timestamps and retain sufficient resolution for post-operation analysis.

---

# Interoperability

PhaseLock is designed to avoid vendor lock-in.

Interfaces should be documented and hardware should be replaceable where practical.

The architecture should support:

- Multiple sensor manufacturers.
- Multiple pump technologies.
- Multiple valve technologies.
- Multiple flight computers.
- Multiple RTOS platforms.
- Multiple simulation environments.
- Multiple telemetry transports.
- Multiple propellant configurations.

---

# Technology Stack

The implementation may use a combination of:

- **Rust** for safety-oriented embedded components.
- **Python** for simulation, testing, and engineering tools.
- **Julia** for advanced scientific and thermodynamic modeling where appropriate.
- **Zephyr RTOS** for supported embedded controllers.
- **RTEMS or real-time Linux** for suitable higher-performance computing platforms.
- **Modelica** for thermodynamic system modeling.
- **CasADi and acados** for predictive-control development.
- **ROS 2 and DDS** where their communication architecture is appropriate.
- **ONNX Runtime** for supported machine-learning inference.
- **TimescaleDB or InfluxDB** for telemetry analysis.
- **Plotly Dash or Streamlit** for engineering and operations visualization.

Specific technology choices remain implementation-dependent and may be replaced when a different technology provides better reliability, determinism, portability, or mission suitability.

---

# Development Principles

PhaseLock development follows these principles:

- Modular architecture.
- Local-first operation.
- Hardware interoperability.
- Deterministic safety.
- Human oversight.
- Reproducible testing.
- Simulation before deployment.
- Hardware-in-the-loop validation.
- Explicit operating states.
- Fault tolerance.
- Vendor independence.
- Documented interfaces.
- Replaceable components.
- Separation of safety and optimization.
- Continuous verification.

---

# Relationship with ForwardState

PhaseLock and ForwardState are complementary systems.

**PhaseLock** manages the physical cryogenic conditioning and transfer infrastructure.

**ForwardState** provides predictive intelligence and higher-level control.

The relationship can be represented as:

PhaseLock → Sensors → ForwardState → Predictions and Control Decisions → PhaseLock Actuators

ForwardState can continuously evaluate the expected future state of the conditioning loop while PhaseLock provides the physical mechanisms required to achieve and maintain that state.

ForwardState repository:

[https://codeberg.org/RoxanneA/ForwardState](https://codeberg.org/RoxanneA/ForwardState)

PhaseLock repository:

[https://gitlab.com/Roxanne_Ardary/phaselock](https://gitlab.com/Roxanne_Ardary/phaselock)

---

# Plugin Development

Plugins should:

- Use documented interfaces.
- Remain modular.
- Avoid modifying safety-critical core logic.
- Declare required dependencies.
- Declare supported hardware.
- Declare supported propellants.
- Provide configuration schemas.
- Provide tests.
- Provide documentation.
- Provide failure behavior.
- Respect configured safety limits.
- Remain independently disableable.

A plugin failure must not compromise the deterministic Core Safety Module.

---

# Testing Requirements

New functionality should include appropriate tests.

Testing may include:

- Unit testing.
- Integration testing.
- Simulation testing.
- Hardware-in-the-loop testing.
- Fault-injection testing.
- Thermal-model validation.
- Pressure-model validation.
- Flow-model validation.
- Sensor validation.
- Actuator validation.
- Regression testing.
- Monte Carlo testing.

Safety-critical changes require additional validation appropriate to the affected subsystem.

---

# Documentation

Changes should be documented in the appropriate project documentation.

Documentation should cover:

- Architecture.
- Interfaces.
- Configuration.
- Operating states.
- Safety behavior.
- Failure behavior.
- Testing.
- Hardware requirements.
- Plugin requirements.
- Integration requirements.

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
  - [https://roxanneardary.com/phaselock/](https://roxanneardary.com/phaselock/)

---

## License & Notice Requirements

PhaseLock is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**. 
- PhaseLock specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request. 
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file. 
