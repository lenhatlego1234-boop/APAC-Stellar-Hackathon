# ChainSensor Oracle

## Project Title
ChainSensor Oracle

## Project Description
ChainSensor Oracle is a decentralized physical infrastructure network (DePIN) and oracle platform built on the Stellar blockchain using the Soroban SDK. It securely bridges physical environmental data—such as air quality (PM2.5), temperature, and humidity collected by microcontroller nodes (ESP32/Arduino)—directly to the blockchain. This ensures that real-world environmental metrics are logged transparently, immutably, and are readily available for other smart contracts to consume.

## Project Vision
The vision of ChainSensor Oracle is to create a trustless, crowdsourced network of environmental data. By eliminating centralized databases, it allows researchers, automated smart cities, and climate-focused decentralized applications (dApps) to access verifiable, real-time climate metrics directly from hardware sensors, fostering a transparent ecosystem for environmental monitoring and automated carbon credit calculations.

## Key Features
- **Data Anchoring:** Securely logs physical sensor readings (e.g., analog/digital data from MQ135 or DHT22) onto the blockchain.
- **Node Whitelisting:** Admin-controlled registration for verified IoT nodes to prevent spam or malicious data injection.
- **Immutable Timestamping:** Every sensor reading is permanently recorded with a blockchain timestamp for verifiable auditing.
- **On-Chain Oracle Access:** Provides a secure interface for other Soroban smart contracts to query the latest environmental data.
- **Tamper-Proof Ecosystem:** Hardware tampering is mitigated by ensuring data integrity from the edge device to the ledger.

## Usage Instructions
1. **Initialize Contract:** Deploy the contract and set the administrator account.
2. **Register Node:** The admin registers a specific hardware device ID (e.g., `ESP32_AQI_STATION_1`).
3. **Push Data:** The physical IoT device uses an API gateway or direct client to push serialized sensor data to the `update_metrics` function.
4. **Query Data:** Third-party dApps or users call the `get_latest_metrics` function to retrieve the most recent air quality or temperature data.
5. **Audit History:** Researchers can scan the blockchain ledger to extract the historical data pattern of any registered sensor.

## Future Scope
- **Tokenized Incentives:** Issue Soroban-based utility tokens to reward users who run active, calibrated sensor nodes (DePIN model).
- **Cryptographic Hardware Signatures:** Implement ECDSA or Ed25519 signature verification directly on the ESP32 to ensure data originates from the exact hardware module.
- **Aggregated Data Feeds:** Calculate the average metrics of multiple sensors in a geographical area directly on-chain.
- **Web Dashboard:** Build a decentralized frontend (dApp) to visualize real-world maps overlaying the blockchain sensor data.

## Technology Stack
- **Rust and Soroban SDK** for high-performance and secure smart contract logic.
- **Stellar Blockchain** for fast, micro-transaction friendly decentralized storage.
- **C/C++ & IoT Protocols** for programming the physical sensor endpoints.

## Contribution
Contributions are encouraged from embedded systems engineers, PCB designers, and Rust developers. Whether you are building the physical nodes or optimizing the Soroban contract, please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License.

### Contract Detail
ID: CB7ZVXDKLDGUAW3H5CAKZXIURM64TNPXMVZGG6EZOHPVXHUGZNBLWXYZ
