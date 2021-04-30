# HealthFog
An ensemble deep learning based smart healthcare system for automatic diagnosis of heart diseases in integrated IoT and Fog computing environments
<div align="center">
<img src="https://github.com/Cloudslab/HealthFog/blob/master/HeartModel/fog-arch.jpg" width="700" align="middle">
</div>

## Quick installation guide
HealthFog uses a master-slave design as shown in the figure above. To setup HealthFog in your fog environment follow these steps:
<b>Note:</b> You need atleast two windows/linux systems with python 3. Follow the following steps in each fog node (master and worker):
1. Install [xampp](https://www.apachefriends.org/xampp-files/7.2.30/xampp-windows-x64-7.2.30-0-VC15-installer.exe) and run Apache server in windows or use <i>Install-scripts/fogbus-install-generic.sh</i> script in a linux device.
2. Clone HealthFog repo at <i>C:/xampp/htdocs/</i> (in windows) or <i>var/www/html/</i> (in linux) and rename the folder as *HealthFog*.
3. Change directory to the HealthFog repo folder.
4. Run ```python3 -m pip install -r requirements.txt```.
5. Run ```cd HeartModel && python3 MasterInterface.py```.
6. Run Apache service from Xampp control panel.
Follow these steps in master node:
1. Update <i>config.txt</i> with IP addresses of all worker nodes (each in a new line) after the first line of 'EnableMaster DisableAneka'. 
2. If connected to cloud using VPN add cloud virtual IP, otherwise add public IP addresses in <i>cloud.txt</i> (each in a new line).

Now download and install <i>Android/FastHeartTest.apk</i> in an android device and enter master IP address to begin healthcare analysis!


## Cite this work
```
@article{tuli2020healthfog,
  title={{HealthFog: An ensemble deep learning based Smart Healthcare System for Automatic Diagnosis of Heart Diseases in integrated IoT and fog computing environments}},
  author={Tuli, Shreshth and Basumatary, Nipam and Gill, Sukhpal Singh and Kahani, Mohsen and Arya, Rajesh Chand and Wander, Gurpreet Singh and Buyya, Rajkumar},
  journal={Future Generation Computer Systems},
  volume={104},
  pages={187--200},
  year={2020},
  publisher={Elsevier}
}
