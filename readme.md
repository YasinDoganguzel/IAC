   # Azure Infrastructure Lab

This project sets up a **hub-and-spoke virtual network topology**, configures **routing, load balancing, and application gateway** in Azure. It includes the deployment of virtual machines, route tables, and advanced network configurations for efficient traffic management.

## 🚀 Tasks Implemented

### Task 1: Provision Infrastructure
1. **Created a Hub-and-Spoke Network Topology** with three VNets (`Hub`, `Spoke1`, `Spoke2`).
2. **Deployed Virtual Machines** (`az104-06-vm0`, `az104-06-vm1`, `az104-06-vm2`, `az104-06-vm3`).
3. **Configured Network Security Groups (NSG)** to control inbound and outbound traffic.
4. **Established Peering** between the VNets to enable communication.

### Task 2: Configure the Hub and Spoke Network Topology
- **Established VNet Peering** between hub and spoke networks.
- **Configured Network Security Groups (NSG)** to manage traffic.
- **Verified connectivity** between hub and spoke VNets.

### Task 3: Test Transitivity of Virtual Network Peering
- **Checked direct and indirect communication** between VNets.
- **Verified routing behavior** to confirm transitivity.
- **Tested connectivity** using Azure Network Watcher.

### Task 4: Configure Routing in the Hub-and-Spoke Topology
1. **Enabled IP Forwarding** on `az104-06-vm0` to act as a router.
2. **Configured User-Defined Routes (UDRs)** for traffic between Spoke VNets.
3. **Tested Routing** using Azure Network Watcher.

### Task 5: Implement Azure Load Balancer
- **Deployed a Public Load Balancer (`az104-06-lb4`)** for distributing traffic.
- **Configured Frontend IP, Backend Pool, and Load Balancing Rules**.
- **Added Health Probes** to monitor VM availability.
- **Tested Load Balancer** by verifying round-robin distribution.

### Task 6: Implement Azure Application Gateway
- **Created a Dedicated Subnet (`subnet-appgw`)** for the Application Gateway.
- **Deployed an Application Gateway (`az104-06-appgw5`)** with Public IP.
- **Configured Backend Pools** to distribute traffic between `az104-06-vm2` and `az104-06-vm3`.
- **Set Up Routing Rules** for efficient request handling.
- **Tested Application Gateway** by verifying traffic distribution.

## 📌 Lessons Learned
- **Hub-and-Spoke Network Design:** Implementing scalable network topologies.
- **User-Defined Routing (UDR):** Configuring custom routes for inter-VNet communication.
- **Azure Load Balancer:** Managing VM traffic efficiently.
- **Application Gateway:** Handling HTTP-based routing.
- **Network Security & Peering:** Ensuring secure and efficient connectivity.
- **Traffic Monitoring:** Using Azure Network Watcher for troubleshooting.

## 🏗️ How to Apply the Terraform Code
1. **Initialize Terraform:**
   terraform init
2. **Plan Deployment:**
   terraform plan
3. **Apply Configuration:**
   terraform apply

This project provides hands-on experience in **Azure networking, security, and traffic management**, ensuring efficient and scalable infrastructure deployment.

