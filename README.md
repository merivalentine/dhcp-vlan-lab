
---

### home lab network setup 🖥️💻🌐

---

![tumblr_dc4e8b24b123bd311b97fc7f39a93f7f_588eb19f_250](https://github.com/user-attachments/assets/2ee2d70a-efac-4722-84fb-36e96331d658)

hii! ![jtql3t](https://github.com/user-attachments/assets/fcf96b41-fce6-43d0-acc8-8584a91e7133)
  
welcome to my home lab network setup! this project was all about setting up a basic network with multiple devices and configuring both wired and wireless connections using cisco devices in packet tracer. i’ll take you through the process of what i did step by step.

---

### project overview ![a5s5oa](https://github.com/user-attachments/assets/b3ba727d-bd8f-4203-8de5-b9fbe31cdbce) 


the goal of this project was to create a small home network with a mix of wired and wireless connections, ensuring communication between the devices. here's a list of the devices that i worked with: ![0y1k3b](https://github.com/user-attachments/assets/5000c274-f67c-4d4f-a564-42f97f5d9d41)


- 3 pcs (pc1, pc2, pc3)  
- 1 printer  
- 1 laptop  
- 1 switch (cisco 2960)  
- 1 router (cisco 2911)  
- 1 wireless router (cisco wt300)  

i connected these devices, configured ip addresses, and set up both dhcp and routing to ensure seamless communication within the network.

![image](https://github.com/user-attachments/assets/17782af0-2617-42d6-92fb-70bcd0304d41)

---

### step-by-step setup 🔧

1. **adding devices 🖥️**  
   the first step was to add all the devices to the packet tracer workspace. i added:  
   - 3 pcs (named pc1, pc2, pc3)  
   - 1 printer  
   - 1 laptop  
   i made sure to rename each device so i could easily identify them later.

2. **adding networking devices 🌐**  
   next, i added the networking hardware required to connect everything:  
   - 1 router: i used a cisco 2911 router for this setup. this router will manage routing between the wired and wireless networks.  
   - 1 switch: a cisco 2960 switch was added to connect all the wired devices in the network (pc1, pc2, pc3, printer).  
   - 1 wireless router: a cisco wt300 wireless router was used to provide wireless connectivity for the laptop.

   ![Screenshot 2025-03-08 172150](https://github.com/user-attachments/assets/41d4fd18-5da7-4010-a28d-ee731c148da9)

3. **connecting the devices 🔌**  
   once the devices were added, i connected them:  

   **wired connections**: i used straight-through cables to connect the pcs, printer, and switch. a straight-through cable is used to connect devices like pcs or switches to other devices like switches or routers.  
   - pc1 → switch  
   - pc2 → switch  
   - pc3 → switch  
   - printer → switch  

   **router and switch**: i connected the router’s ethernet port to the switch using a straight-through cable to allow the router to communicate with the pcs and printer.  

   **router and wireless router**: the router and the wireless router were connected using a crossover cable to ensure that the wireless router could access the router’s resources and provide wireless connectivity.

   ![Screenshot 2025-03-08 172621](https://github.com/user-attachments/assets/f347ff52-4956-4caa-a8fb-d9a5ffdbc7ed)  
   ![Screenshot 2025-03-08 172853](https://github.com/user-attachments/assets/8ce38461-f63f-4c3b-86d1-53f85ec03906)

4. **assigning ip addresses 📶**  
   for all the devices to communicate correctly, i assigned static ip addresses. here’s the ip structure i used:  

   **wired network (using ip range 192.168.1.0/24)**:  
   - pc1: 192.168.1.2  
   - pc2: 192.168.1.3  
   - pc3: 192.168.1.4  
   - printer: 192.168.1.5  

   **wireless network (using ip range 192.168.2.0/24)**:  
   - laptop: 192.168.2.2  

   **router**: i assigned the router two ip addresses for the two networks:  
   - ethernet interface (wired): 192.168.1.1  
   - wireless interface: 192.168.2.1  

5. **configuring dhcp and routing 📡**  
   once the devices were connected and assigned ip addresses, i moved on to configuring the router and wireless router.  
   - **dhcp**: i enabled dhcp on the router to automatically assign ip addresses to the devices within both networks. this was done for both the wired (192.168.1.0/24) and wireless (192.168.2.0/24) subnets.  
   - the router’s dhcp configuration provided ips for the wired network (range: 192.168.1.2 - 192.168.1.254) and the wireless network (range: 192.168.2.2 - 192.168.2.254).  
   - **routing configuration**: to enable communication between the two subnets, i configured routing on the router to route traffic between the 192.168.1.x and 192.168.2.x networks.

   ![Screenshot 2025-03-08 174101](https://github.com/user-attachments/assets/d702162f-8016-461d-b778-9e587941ccdb)  

   i used a static route to ensure devices on the wired network could communicate with the wireless network and vice versa. the router was set to route traffic from the 192.168.1.0/24 network to 192.168.2.0/24 and vice versa.  
   - **router interface configuration**: i also made sure to enable both router interfaces by entering `no shutdown` on each interface to activate them.

6. **testing connectivity 🧪**  
   once all the configurations were in place, i tested the network to make sure everything was working correctly:  
   - i pinged from pc1 to pc2, pc3, and the printer to confirm that devices on the wired network could communicate with each other.  
   - i pinged from the laptop to the printer and pc1 to ensure that the wireless and wired networks could communicate through the router.  
   all pings were successful, confirming that the network was set up properly.

   ![Screenshot 2025-03-08 184126](https://github.com/user-attachments/assets/1a714eaf-2b15-4fd2-85f7-9db813737f3e)  
   ![Screenshot 2025-03-08 184126](https://github.com/user-attachments/assets/ddee6457-9df0-46db-aab7-f8fd98e625c3)  
   ![Screenshot 2025-03-08 184126](https://github.com/user-attachments/assets/7b08dec8-2cde-4085-adc1-84387992821f)  
   ![Screenshot 2025-03-08 184203](https://github.com/user-attachments/assets/06de0270-a7e1-4e15-90ad-57e81bb34ea9)  
   ![Screenshot 2025-03-08 183938](https://github.com/user-attachments/assets/e3a23163-3505-451d-9468-cb8444a13249)  
   ![Screenshot 2025-03-08 184024](https://github.com/user-attachments/assets/72e0610e-3d11-458b-8b4e-0c13291b3c0f)  
  

---

### key configuration details 📚

**router ips**:
- ethernet interface: 192.168.1.1  
- wireless interface: 192.168.2.1  

**dhcp configuration**:
- the router assigned ips for the wired network (range: 192.168.1.2 - 192.168.1.254) and the wireless network (range: 192.168.2.2 - 192.168.2.254).

**routing**:
- static routes were set on the router to enable communication between the 192.168.1.0/24 and 192.168.2.0/24 networks.

---

this simple setup demonstrates how to connect and configure a basic home network with both wired and wireless connections. by assigning ip addresses, enabling dhcp, and configuring routing, i was able to ensure that all devices could communicate seamlessly within the network.

thats all, thank you for reading  ![lv0nhk](https://github.com/user-attachments/assets/5758c235-e8d2-4aba-b1cd-b617a7a82fd5)
 
![tumblr_e0c744a762ef1ecc3eacda2206683585_ac531a94_250](https://github.com/user-attachments/assets/336a8cc4-316d-46e4-ae4a-360eb22a3d5e)
 ![uv2o1k](https://github.com/user-attachments/assets/ea4eae2b-1dbf-4a34-b932-2f3a3b34187e)


---
