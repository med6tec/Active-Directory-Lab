## Introduction
In this lab, I will simulate the installation of a Windows Server 2019 machine and configure ADDS on it to become a Domain Controller.
# AD Lab Requirements:
VMware Workstation Pro

Windows Server 2019 ISO

Windows 10 ISO
## Setting Up the Domain Controller
1. Open VMware Workstation Pro > File > New VM > Enter a name for the VM > Select Microsoft Windows as the Type > Select Windows 2019 (64-bit) as the Version > Next

![Capture 0](https://github.com/user-attachments/assets/4bdaf3e0-6890-4042-b0a0-75515fc0c8c6)
![Capture 1](https://github.com/user-attachments/assets/b4179d75-46e8-4124-8c56-94f2f344f389)

2. Specify a destination path for the VM > Create a Hard Disk & set the size to 50 GB

![Capture 2](https://github.com/user-attachments/assets/da8f47d0-1af3-42ab-b55a-4b9c4135606d)
![Capture 3](https://github.com/user-attachments/assets/7e6da549-ffe7-48c2-8f47-ee6d9c8a0db5)

3. Mount the ISO file
![Capture 4](https://github.com/user-attachments/assets/2384d198-6eb1-441f-9336-c9d22cd8f62d)

4. Now our VM is ready!!!
![Capture 5](https://github.com/user-attachments/assets/66bfef65-8f19-47bb-80ee-6b570b0debdd)

## Windows Server 2019 installation steps:
1. Start up the VM, choose your preferred settings and click Next > Install now.
![Capture 7](https://github.com/user-attachments/assets/b2e47a5a-85ef-4af9-a30c-bc9cd38e57e0)
![Capture8](https://github.com/user-attachments/assets/2e7781ba-742b-4105-a02c-77f500be336c)


2. Select Windows Server 2019 Datacenter Evaluation (Desktop Experience) > Next > Tick the license terms > Next

![Capture9](https://github.com/user-attachments/assets/44adf0f0-2255-4368-a81b-dcb224ab3696)

![Capture10](https://github.com/user-attachments/assets/9cd687e8-49c7-4f71-a4c6-4d10f3c1ba40)

3. Select, Custom: Install Windows only (advanced).

![Capture11](https://github.com/user-attachments/assets/59830798-3abe-4a09-a369-1ed3bd16258c)

![Capture13](https://github.com/user-attachments/assets/95143d6f-68c5-4b0c-bf2a-8ca3f1577989)

4. After successful installation, enter a password > Finish. Then enter the password to login after finalization.

![Capture14](https://github.com/user-attachments/assets/6eb0f72d-c65f-42d5-9bf3-3f61fa5677d0)

5. Log in as the Administrator, and you’ll be greeted with the welcoming sight of Server Manager.

![15](https://github.com/user-attachments/assets/7b297248-49fc-4278-8067-c3237dbaa72d)

## Windows Server 2019 Configuration steps:

1. Rename the PC (Computer Name > Change) & Restart the machine.

![Capture16](https://github.com/user-attachments/assets/e4df950d-921a-40a0-ad15-3f471480c825)

2. Change date and time + time zone & Configure a static IP address.

![Capture17](https://github.com/user-attachments/assets/a4038e9c-aa7e-494c-9e84-1df41eb813e6)

3. Install Active Directory Domain Services:

While navigating through Server Manager, head to the top-left corner and click on ‘Manage.’ From there, select ‘Add Roles and Features.

![Capture19](https://github.com/user-attachments/assets/4679d2a1-083c-4a4b-82a2-581aaf4782ad)

When prompted, choose the ‘Role-based or feature-based installation’ option, and then select the suitable server from the available pool.

![](https://miro.medium.com/v2/resize:fit:640/format:webp/1*2WcUle8cRhCdywuvRZVMnQ.png)

Next, go ahead and select ‘Active Directory Domain Services’ from the list of available options. Click ‘Next’ to proceed through the installation prompts.

![Capture20](https://github.com/user-attachments/assets/e0ad2ff0-b8be-41fe-887f-f947460b71ef)

![Capture21](https://github.com/user-attachments/assets/b7257419-1c48-44ac-8b2a-19b4c30e65c5)

After the installation is complete, it’s time to wrap up the post-deployment tasks by promoting this server to a Domain Controller.

![Capture22](https://github.com/user-attachments/assets/4f5e7b55-eb6b-4ecc-94a6-f9c810478729)

Naming my root domain as ‘rabat.local’

![Capture23](https://github.com/user-attachments/assets/7ff324c6-51d9-4d97-ad99-77098018e916)

![Capture24](https://github.com/user-attachments/assets/ee964bae-2dba-4288-8b31-b801f5b95505)

![Capture25](https://github.com/user-attachments/assets/b229e846-0473-431e-a941-fc846cd81be9)

Now, a restart is required. Upon restarting your system, you’ll be greeted by a wonderful login screen.

![Capture26](https://github.com/user-attachments/assets/89e742b5-b18f-4689-95c0-51845c406dae)
