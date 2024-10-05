# MOB-API Smoke Test Proof of Concept

## Overview

This project serves as a Proof of Concept (PoC) for performing smoke tests on the MOB-API backend platform. The goal is to achieve 100% coverage of all endpoints while incorporating lightweight performance tests to monitor and identify potential areas for improvement.

## Project Objectives

1. **Endpoint Coverage:** Test all MOB-API endpoints to ensure they function correctly. This includes checking for response statuses, payloads, and key data points.
2. **Performance Monitoring:** Run small-scale performance tests to monitor response times, latency, and throughput, which helps identify potential bottlenecks.
3. **Scalability Assessment:** Evaluate the feasibility of extending these tests into a full-fledged testing suite, providing insights into areas that may require optimization.

## Project Structure

```
mob-api-smoke-test/
│
├── tests/
│   ├── functional/
│   ├── performance/
│   └── utils/
│
├── reports/
│   └── [performance and test result reports]
│
├── config/
│   ├── environment_config.json
│   └── endpoint_config.json
│
├── README.md
├── requirements.txt
└── run_tests.py
```

- **`tests/`**: Contains all test scripts, divided into functional and performance tests.
- **`reports/`**: Stores test result reports and logs for performance analysis.
- **`config/`**: Holds configuration files for environment and endpoint settings.
- **`requirements.txt`**: Lists all Python dependencies required for the project.
- **`run_tests.py`**: Main script to execute tests.

## Prerequisites

Ensure you have Python 3.x and the following dependencies installed:

```bash
pip install -r requirements.txt
```

Additional setup steps:
- Update the `environment_config.json` file with your environment details (e.g., base URL, authentication tokens).
- Update the `endpoint_config.json` file with all MOB-API endpoints you plan to test.

## Usage

To execute the smoke tests, run the following command:

```bash
python run_tests.py --type [functional|performance|all]
```

- **Functional Tests:** Run to validate the basic functionality of each endpoint.
- **Performance Tests:** Run to measure response times and identify potential areas for improvement.
- **All:** Run both functional and performance tests sequentially.

### Example Commands

Run functional tests only:

```bash
python run_tests.py --type functional
```

Run performance tests only:

```bash
python run_tests.py --type performance
```

Run both functional and performance tests:

```bash
python run_tests.py --type all
```

## Reporting

Upon completion, test results and performance reports will be stored in the `reports/` directory. The reports will provide detailed insights into endpoint status, response times, and potential bottlenecks.

## Contributing

This PoC is a starting point and may evolve. If you have suggestions or would like to contribute:
- Fork this repository
- Make changes
- Submit a pull request

## Future Enhancements

Potential areas for future development:
- **Increased Test Coverage:** Extend coverage to include edge cases and error conditions.
- **Full Performance Suite:** Scale up the performance tests to simulate higher loads.
- **Continuous Integration (CI):** Integrate with CI/CD tools for automated testing on every deployment.
