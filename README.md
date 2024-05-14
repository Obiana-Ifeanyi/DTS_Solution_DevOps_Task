# Ansible Docker Project

This project demonstrates the use of Ansible for automating the deployment of a Dockerized application stack. The project structure includes playbooks, inventory files, and Docker setup scripts.

## Project Structure
```
└── ansible-docker-project/
    ├── ansible/
    │   ├── inventory.yml
    │   ├── playbook.yml
    │   ├── deploy_stack_playbook.yml
    │   └── lab/
    │       ├── app.js
    │       ├── Dockerfile
    │       ├── docker-compose.yml
    │       ├── package.json
    │       └── node_modules
    ├── scripts/
    │   └── install_docker.sh
    └── README.md
```

### Directory Details

- **ansible/**: Contains Ansible playbooks and configuration files.
  - **inventory.yml**: Specifies the hosts for Ansible to manage.
  - **playbook.yml**: The main playbook for general configurations and setups.
  - **deploy_stack_playbook.yml**: A playbook specifically for deploying the Docker stack.
  - **lab/**: Contains the application to be deployed.
    - **app.js**: Main application file.
    - **Dockerfile**: Docker configuration for the application.
    - **docker-compose.yml**: Docker Compose file to set up the application stack.
    - **package.json**: Node.js package configuration.
    - **node_modules/**: Directory containing installed Node.js modules.

- **scripts/**: Contains utility scripts.
  - **install_docker.sh**: A script to install Docker on the target machine.

## Getting Started

### Prerequisites

- Ansible installed on the control machine.
- Docker and Docker Compose installed on the target machine(s).

### Installation

1. **Install Docker**:
   Run the following script to install Docker on your target machine(s):

   ```bash
   chmod +x install_docker.sh
   bash ./install_docker.sh

2. **Setup Ansible Inventory:**
   Define your target machines in the ansible/inventory.yml file.

3. **Run Ansible Playbook:**
   Execute the Ansible playbook to set up your environment and deploy the Docker stack:

   ```bash
   ansible-playbook -i ansible/inventory.yml ansible/deploy_stack_playbook.yml

## Application Details

- app.js: This is the main Node.js application file located in the ansible/lab/ directory.
- Dockerfile: Used to build the Docker image for the application.
- docker-compose.yml: Defines the Docker services, networks, and volumes for the application stack.

## Usage
After running the Ansible playbook, the Docker stack will be up and running. You can manage the stack using Docker Compose commands.

1. **To view the running services:**
   
   ```bash
   ansible-playbook -i ansible/inventory.yml ansible/deploy_stack_playbook.yml

2. **To stop the services:*

   ```bash
   ansible-playbook -i ansible/inventory.yml ansible/deploy_stack_playbook.yml

## Contributing
Contributions are welcome! Please submit a pull request or open an issue to discuss your ideas.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
This project was inspired by the need to automate the deployment process for containerized applications using Ansible and Docker.
