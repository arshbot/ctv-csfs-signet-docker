# CTV and CSFS Enabled Bitcoin Node

A Docker-based Bitcoin node configured with CheckTemplateVerify (CTV) and CheckSigFromStack (CSFS) capabilities enabled. This node runs on a special signet (MutinyNet) that allows developers to test and build applications using these proposed Bitcoin protocol upgrades.

## What are CTV and CSFS?
- **CheckTemplateVerify (CTV)**: A proposed Bitcoin upgrade that enables covenant-style contracts by allowing you to restrict how bitcoins can be spent in the future.
- **CheckSigFromStack (CSFS)**: A proposed opcode that allows signature verification against arbitrary messages, enabling more flexible smart contract designs.

## Quick Start

1. Clone this repository:
   ```bash
   git clone https://github.com/arshbot/ctv-csfs-signet-docker
   cd ctv-csfs-signet-docker
   ```

2. Set up environment variables:
   ```bash
   cp .env.example .env
   ```

3. Start the node:
   ```bash
   docker-compose up -d
   ```

## System Requirements
- Apple Silicon Mac (M1/M2/M3) or x86_64 systems
- Docker and docker-compose
- ~1GB of disk space (running in pruned mode)

## Node Configuration
The node runs as a Docker container with the following exposed ports:
- 28332-28334: RPC and P2P ports
- 38332-38334: Additional network ports

Environment variables in `.env`:
- `RPCPASSWORD`: Password for RPC access
- `PRIVKEY`: Node private key
- `SIGNETCHALLENGE`: Signet challenge
- `EXTERNAL_IP`: Your node's external IP (if running as a public node)

## Connecting to the Node
RPC connection details:
- Host: localhost
- Port: 38332 (RPC)
- Network: signet

## Technical Details
This node runs on MutinyNet, a specialized Bitcoin signet that has both CTV and CSFS activated. This makes it perfect for:
- Developing and testing covenant-based applications
- Experimenting with new smart contract designs
- Prototyping applications that rely on these proposed Bitcoin upgrades

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
[Insert License Information]
