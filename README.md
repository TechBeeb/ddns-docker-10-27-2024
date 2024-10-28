# DDNS Updater with Docker

This repository contains the configuration files (`config.yaml` and `data/config.json`) necessary to set up a Dynamic DNS (DDNS) updater using Docker. The setup utilizes Cloudflare as the DNS provider to automatically update DNS records whenever your IP address changes, ensuring seamless access to your home network.

## Prerequisites
- Docker installed on your system
- Cloudflare-managed domain

## Files
- `compose.yaml`: Docker Compose configuration for setting up the `ddns-updater` container.
- `data/config.json`: Configuration for the DDNS service, including Cloudflare API token and zone identifier.

## Setup Instructions
1. **Clone the Repository**:  
   ```sh
   git clone <repository-url>
   cd ddns-updater
   ```
2. **Edit Configurations**: Update `config.json` with your specific Cloudflare token, zone identifier, and domain details.

3. **Start Docker Container**:  
   ```sh
   docker compose up --build -d
   ```

## How It Works
The Docker container will run the DDNS updater service, which connects to Cloudflare and updates the IP address of your configured domain automatically. The `ddns-updater` container uses the details in `config.json` to communicate with Cloudflare's API.

## Useful Resources
For a detailed guide on setting up DDNS, see [My Journey with DDNS](https://techbeeb.com/posts/Journey-with-DDNS/).

## License
This project is licensed under the CC BY 4.0 license. See the LICENSE file for details.