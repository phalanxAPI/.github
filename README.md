# Phalanx 

## Overview

The Phalanx is a sophisticated system designed for robust API management, security scanning, and microservice orchestration. This project integrates several key components, including a Next.js and Mantine-powered frontend dashboard, a MongoDB database, and a suite of microservices managed by the Phalanx enterprise server.

## Project Architecture

### 1. Dashboard (Frontend)
- **Technology:** Next.js, Mantine
- **Repository:** [Dashboard Repo](https://github.com/phalanxAPI/dashboard.git)
- **Description:** The dashboard serves as the user interface for interacting with the system, providing real-time insights and control over various services. Built with Next.js for server-side rendering and Mantine for a rich UI component library, the dashboard offers an intuitive and responsive experience.
- **Commands to Run:**
  ```bash
  git clone https://github.com/phalanxAPI/dashboard.git
  cd dashboard
  bun i
  bun dev
### 2. Database
- **Technology:** MongoDB
- **Description:** MongoDB is used as the database to store all necessary data, including service logs, user information, and scan reports. Its flexible schema design allows for efficient handling of large and unstructured datasets, making it ideal for this project.

### 3. Phalanx Enterprise Server
- **Description:** The Phalanx enterprise server is the backbone of the system, running all microservices and managing their interactions. It ensures that each component operates seamlessly within the broader infrastructure, handling API requests and processing data as needed.

### 4. Scout
- **Function:** Security Scanning and Reporting
- **Repository:** Scout Repo
- **Description:** Scout is responsible for scanning the entire application for vulnerabilities. It performs security checks across various layers of the system, generating detailed reports that highlight potential risks and recommend remediation steps.
- - **Commands to Run:**
  ```bash
  git clone https://github.com/phalanxAPI/scout.git
  cd scout
  bun install
  bun run index.ts
### 5. Lighthouse
- **Function:** Microservice Management and Orchestration
- **Repository:** Lighthouse Repo
- **Description:** Lighthouse orchestrates the microservices, ensuring smooth communication and operation. It interacts directly with the Commander dashboard to provide a cohesive management experience. Lighthouse also coordinates the other microservices—Navigator, Sysmon, Inbound, and Outbound—ensuring they function together effectively.
- - **Commands to Run:**
  ```bash
  git clone https://github.com/phalanxAPI/lighthouse.git
  cd lighthouse
  pnpm i
  pnpm dev:commander
  pnpm dev:inbound
  pnpm dev:outbound
  pnpm dev:navigator
  pnpm dev:sysmon
 
#### Subcomponents:
- **Commander:** Central control hub that interacts with the dashboard, providing an interface for managing all services.
- **Navigator:** Handles routing and efficient management of API requests, ensuring that each request reaches the correct service.
- **Sysmon:** Monitors the system’s health, collecting and analyzing performance metrics to ensure smooth operation.
- **Inbound:** Manages incoming API requests, processing them securely and efficiently.
- **Outbound:** Handles outgoing data requests, ensuring secure and reliable data transmission between the client and server.

### 6. Client Interaction
- **Description:** The four microservices (Navigator, Sysmon, Inbound, Outbound) interact with clients through the Phalanx enterprise server. This interaction allows for secure and efficient data exchange, ensuring the smooth operation of all services.

