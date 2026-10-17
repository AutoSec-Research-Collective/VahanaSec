# VahanaSec

**An open-source automotive security research and simulation lab by ARC.**

**Simulate. Investigate. Secure.**

VahanaSec aims to provide a modular, reproducible environment for learning and experimenting with automotive cybersecurity concepts using simulated vehicle networks and defensive security controls.

The project is being developed as part of the AutoSec Research Collective (ARC).

> **Project status:** Early-stage development. Features described as planned are not necessarily implemented. Check the repository's issues, releases, and documentation for the current state.

## Why VahanaSec?

Modern vehicles combine embedded controllers, in-vehicle networks, diagnostic services, mobile applications, telematics, and cloud-connected systems. Understanding their security requires practical experiments as well as theoretical knowledge.

VahanaSec aims to make those experiments accessible without requiring an actual vehicle.

## Project Goals

- Provide a software-only simulated vehicle environment.
- Demonstrate communication between virtual electronic control units (ECUs).
- Generate and inspect synthetic in-vehicle network traffic.
- Explore message validation, replay detection, and anomaly detection.
- Build repeatable test scenarios for defensive controls.
- Provide accessible documentation and educational exercises.
- Establish a foundation for future automotive security research modules.

## Planned Architecture

The initial lab is intended to contain:

- **Vehicle Simulator:** Coordinates the simulated vehicle environment.
- **Body Control Module (BCM):** Represents selected body-related signals and functions.
- **Engine ECU:** Represents a simulated powertrain controller; no real vehicle control is involved.
- **Gateway ECU:** Applies configurable rules to traffic moving between simulated network segments.
- **Virtual CAN Bus:** Carries synthetic messages between simulated components.
- **Security Monitor:** Analyses traffic for configured policy violations and anomalies.
- **Test Suite:** Validates expected behaviour and defensive controls.

These are architectural goals, not claims that every component is already implemented.

## Planned Research Modules

### 1. Network Simulation
Generate, transmit, receive, and inspect synthetic CAN messages within an isolated lab.

### 2. Message Validation
Define expected message identifiers, payload sizes, rates, and basic validation rules for simulated traffic.

### 3. Replay Detection
Explore how a defensive monitor can identify repeated or stale messages using a clearly documented, deterministic test dataset.

### 4. Anomaly Detection
Evaluate simple rule-based baselines and compare them against synthetic normal and anomalous traffic.

### 5. Gateway Security
Experiment with allowlists, network segmentation, and policy enforcement between simulated components.

### 6. Diagnostic Security
Develop educational scenarios around diagnostic access control and defensive validation using simulated services.

### 7. Testing and Reproducibility
Provide automated tests, synthetic datasets, and repeatable experiments so contributors can independently validate results.

## Technology Direction

The initial implementation may use:

- Python for simulation and security logic.
- `python-can` for CAN abstractions and supported virtual interfaces.
- SocketCAN or a virtual CAN interface where supported by the host operating system.
- Pytest for automated tests.
- Docker for reproducible components where appropriate.
- A lightweight web or command-line interface as the project matures.

The exact stack may change based on testing, maintainability, and contributor feedback.

## Getting Started

The initial development setup is being established. Once the first runnable release is available, this section will include verified installation and execution instructions.

Until then:

1. Review the project documentation.
2. Check the current issues and roadmap.
3. Use an isolated development environment.
4. Run only the commands documented for the current implementation.
5. Do not assume planned components are operational.

## Repository Layout

The intended layout will evolve with implementation.

```text
vahanasec/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── SUPPORT.md
├── docs/
│   ├── architecture.md
│   └── roadmap.md
├── src/
│   └── vahanasec/
├── tests/
└── examples/
```

## Safety and Responsible Use

VahanaSec is intended for education, defensive engineering, and authorised research.

- Use simulated or explicitly authorised environments.
- Do not connect experimental components to a real vehicle without a separately reviewed safety plan and appropriate authorisation.
- Do not use the project for vehicle theft, sabotage, unauthorised access, or interference with safety-critical functions.
- Do not upload proprietary firmware, credentials, private keys, personal information, or confidential vehicle data.
- Report potential vulnerabilities according to [SECURITY.md](SECURITY.md).

A successful simulation is not evidence that a control is safe or effective in a production vehicle.

## Contributing

Contributions are welcome, including code, tests, documentation, architecture reviews, and reproducible experiments.

Read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) before participating.

## Roadmap

See [docs/roadmap.md](docs/roadmap.md) for the planned milestones and current project priorities.

## Licence

Unless otherwise stated for a particular component, VahanaSec is intended to be released under the Apache License 2.0. See the root `LICENSE` file for the applicable terms.

Third-party dependencies and contributions remain subject to their own applicable licences and notices.

## About ARC

VahanaSec is a project of the **AutoSec Research Collective (ARC)**, a community-driven initiative focused on automotive cybersecurity research, open-source engineering, and security education.

**Research. Engineer. Secure.**
