<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/5280dd26-5bad-4ee9-8d1d-a31fcece015b" />
in this image here we see in the log file in ubuntu how the machine was attacked several times before using brute force attaks 


<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/1bea6ae6-e6b5-4207-86fa-8d082a03cf83" />
here is a demonstartion of how the attacker was able to make admin level modification on the machine's nginx server which could be lethal in real-woeld senarios 

pinging the victime to see if connection could be established 
<img width="958" height="519" alt="image" src="https://github.com/user-attachments/assets/d841d3d2-f2b1-42c3-a4d2-afc32766896a" />

crucial step!
scanned the victim ip using nmap to see what ports are open 
<img width="964" height="202" alt="image" src="https://github.com/user-attachments/assets/96f64d01-9995-4561-9fe9-2282f3e07495" />

 using brute forcing with hydra to crack the victim's password 
<img width="953" height="517" alt="image" src="https://github.com/user-attachments/assets/9212ad70-985e-4b78-9014-bb24b55ae318" />

taking action on the victim's machine 
<img width="1228" height="261" alt="image" src="https://github.com/user-attachments/assets/5cee7f0d-cf52-44fd-a02e-4d714663d3b6" />
 
 <img width="1211" height="84" alt="image" src="https://github.com/user-attachments/assets/ea81fe0b-2be5-4da5-a338-d2a8e7b79d60" />
the victim could also keep the port open and allow only certain ip addresses
# Allow IP to access specific port
sudo ufw allow from 192.168.1.100 to any port 22


 
