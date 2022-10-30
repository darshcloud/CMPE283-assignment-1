# CMPE 283 - Virtualization Technologies - Assignment 1 - Discovering VMX Features

Professor's Name: Michael Larkin <br/>
Student's Name: Darshini Venkatesha Murthy Nag <br/>
Student ID: 016668951 <br/>

## Steps used to complete the assignment

* Install the VMware Workstation player or VMware Workstation Pro on your Windows machine. <br/><br/>
* Create a Ubuntu VM with virtual disk size 100GB. Customize the hardware settings under the processor tab and check the checkbox Virtualize Intel VT-x/EPT or AMD-V/RVI.<br/><br/>
* Power on the Virtual Machine <br/><br/>
* Open the terminal. To Install git run the below command <br/>
  sudo apt install git<br/><br/>
* Install gcc and make using the below command <br/>
  sudo apt install gcc make<br/><br/>
* Install <br/>
  sudo apt install linux-headers-$(uname -r)<br/><br/>
* Clone the github repository using the below command <br/>
  git clone https://github.com/darshcloud/CMPE283-assignment-1.git <br/><br/>
* Go inside the repository directory and run the following commands to create a new kernel Module with assignment functionality <br/>
  make clean <br/>
  make<br/><br/>
* Insert the new module by running the below command <br/>
  sudo insmod cmpe283-1.ko<br/><br/>
* Verify the output by in the system message log by running the below command<br/>
  sudo dmesg <br/><br/>

Output log of Pinbased Controls
![Picture1](https://user-images.githubusercontent.com/111547793/198863461-e7ffbbf5-af3b-40af-91e6-32bf9b5cb668.png)<br/>

Output log of Primary Procbased controls 
![Picture2](https://user-images.githubusercontent.com/111547793/198863538-97c9a9cc-e383-4170-9d40-d1612c38c8e0.png)<br/>

As Activate Tertiary control bit is not set, The Tertiary Control Capability is unavailable. The Secondary Control Capabilities are as shown below <br/>
Output log of Secondary Procbased Controls
![Picture3](https://user-images.githubusercontent.com/111547793/198863582-1ea46cf8-431b-4f36-972d-ab9882400308.png) <br/>

Output log of Exit controls
![Picture4](https://user-images.githubusercontent.com/111547793/198863636-5e1ec0b2-aae6-45cf-b738-ae2a4eaa33ba.png) <br/>

Output log of Entry controls
![Picture5](https://user-images.githubusercontent.com/111547793/198863643-9882c2e3-b147-4648-ac52-560f577eb685.png) <br/>



 




