# n8n-ansible

## Structure of the `n8n-ansible.zip` Archive

```
n8n-ansible/
├── files/
│   └── docker-compose.yml
├── install_n8n.yml
├── inventory
├── run_n8n_install.sh
```

---

## Overview

A ready-to-use solution for automated installation of **n8n** on a server using **Ansible** and **Docker**.

## What This Project Does

- Installs required packages: Docker, docker-compose, nginx, openssl  
- Creates directories and configuration files for n8n  
- Generates a self-signed SSL certificate  
- Copies settings from `files/docker-compose.yml`  
- Configures nginx reverse proxy (if needed)  
- Launches n8n on port **5678**  
- Performs all actions with a single command  

## Project Contents

```
n8n-ansible/
├── files/
│   └── docker-compose.yml         — Docker container configuration
├── install_n8n.yml                — main Ansible playbook
├── inventory                      — host definition (localhost by default)
├── run_n8n_install.sh             — installation launch script
```

## How to Use

1. Clone or download this repository to your server  
2. Navigate into the folder:

   ```bash
   cd n8n-ansible
   ```

3. Make the script executable:

   ```bash
   chmod +x run_n8n_install.sh
   ```

4. Run the installation:

   ```bash
   ./run_n8n_install.sh
   ```

## Result

After execution, you will have a fully working instance of **n8n**, accessible in your browser at:

```
http://<server_IP>:5678
```

## Who This Is For

- DevOps engineers who want automated deployment  
- Developers who need a quick n8n setup locally  
- Teams using the “infrastructure as code” approach  

With love, **webdoka**
