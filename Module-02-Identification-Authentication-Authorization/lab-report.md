# Module 02 - Identification, Authentication, and Authorization  

## Objective  
This lab focused on implementing Role-Based Access Control (RBAC) in Windows Admin Center (WAC) to restrict user activities and enhance security.  

## Tools Used  
- **PfSense Firewall** – Network security and traffic filtering.  
- **Admin Machine-1** – Primary administrative workstation.  
- **AD Domain Controller** – Manages authentication and authorization.  
- **Web Server** – Target system for RBAC configuration.  
- **Attacker Machine** – Used for security testing and validation.  

## Steps Performed  

### **1. Installing Windows Admin Center (WAC)**  
- Logged into **Admin Machine-1** and navigated to the installation path.  
- Installed Windows Admin Center (WAC) by executing `WindowsAdminCenter1910.msi`.  
- Configured the gateway endpoint and completed the installation.  

### **2. Adding Web Server to WAC for Management**  
- Launched WAC and verified **Admin Machine-1** was listed under "All Connections."  
- Used the **+Add** button to add "Webserver" as a managed resource.  
- Entered **Administrator** credentials to authenticate the connection.  
- Verified Webserver was successfully added to WAC.  

### **3. Configuring Role-Based Access Control (RBAC) in WAC**  
- Navigated to **Settings → Role-based Access Control (RBAC)** in WAC.  
- Applied RBAC configuration and restarted the **WinRM service**.  
- Verified RBAC status changed to **"Applied"** after the update.  

### **4. Assigning Limited Access to User ‘John’**  
- Opened **Local Users & Groups** in WAC.  
- Selected user **John** and modified **Manage Membership** settings.  
- Assigned the **Windows Admin Center Readers** role to John (view-only mode).  

### **5. Testing RBAC Implementation**  
- Logged into Webserver as user **John** using assigned credentials.  
- Verified limited access by attempting to perform administrative actions.  
- Tried to create a **Virtual Hard Disk (VHD)** in the Storage pane → Access Denied.  

## **Outcome**  
✅ Successfully installed **Windows Admin Center (WAC)** and configured **RBAC**.  
✅ User **John** was restricted from unauthorized modifications.  
✅ Access control was validated by an **"Access Denied"** error.  

