# Home Office Solution during the COVID-19 Pandemic using Microsoft Azure VPN Gateway

![picture with the words Cloud Project and icons of the services used](https://miro.medium.com/v2/resize:fit:720/format:webp/0*QN8D9249bT7bgS7O.jpg)

In this real world-based project, I acted as a Cloud Specialist to create a solution for people who were working in the office to start working from home,
normally accessing the environment in Microsoft Azure, and without exposing the entire environment to the internet.

To solve this business problem and come up with a solution compatible with the requirements, I defined that it was necessary to implement Point-to-Site (P2S) 
VPNs, so that employees who were working from home would close an encrypted tunnel between their computer and the Microsoft Azure environment.

![picture showing a graph of the solution architecture](https://miro.medium.com/v2/resize:fit:720/format:webp/0*h3l9qwuXgAww-waI.jpg)

The process as a whole is relatively straightforward, thanks to built-in Azure tools that support those workflows. First I created a virtual network and added 
a virtual machine without a public IP address, which will serve as a connection point to test this project. Next I created a VPN Gateway, which is the bridge
between the client to the virtual network, and added the root certificate (previously created for this project, since it’s a lengthy process), also adding an 
IP pool for the clients on the VPN. After that, I downloaded the VPN installer, created automatically by Azure.

On my local machine I installed the client certificate and the VPN. After this process, I just had to turn on the VPN trough the network panel on Windows. 
I pinged the private IP address on the virtual machine successfully. To make another test, I installed Apache on the virtual machine, which I could access 
normally trough the private IP address. After disconnecting from the VPN, I couldn’t reach the machine anymore.

![Apache opened on a browser window](https://miro.medium.com/v2/resize:fit:720/format:webp/0*aHXojCyBRb9wGjTA.png)

I was positively surprised how quickly Azure allowed me to set up this connection, which flexibilizes companies to answer to emergency situations —
just like what we’ve been trough past years with Covid-19. Besides a quick reaction, the companies and users can still enjoy the security, since their
data is not exposed to the public internet.


