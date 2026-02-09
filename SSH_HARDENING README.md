<img width="674" height="484" alt="image" src="https://github.com/user-attachments/assets/1273eb5d-da4e-432a-b7a2-383f576c4458" />Objective

The purpose of this lab is to secure SSH access by implementing SSH key-based authentication and disabling password authentication, thereby mitigating brute-force attacks.
as we saw before how dangerous are bruteforce attacks and how could they compromise one's machine ! 
to mitigate these threats we could use KEY_BASED_AUTHENTICATION 
to begin we generated ssh key pairs (public and private keys) on the attacker machine to allow us to authenticate without needing a password 

step 1 generate keys 
ssh-keygen -t ed25519 
This generates a private key and public key in the default directory (~/.ssh/).

We left the passphrase empty for this lab, but adding one is recommended for real-world scenarios.
then we copied the public key on ubuntu 
ssh-copy-id username@ubuntu-id 

2: Disable Password Authentication on Ubuntu

To prevent password-based logins and further harden SSH, we disabled password authentication on the Ubuntu server.
steps 

1 edit the configation file 
sudo nano /etc/ssh/sshd_config

2 Disable password authentication:
Modify the file to include these lines:
PasswordAuthentication no
PermitRootLogin no

3 resart ssh 
sudo systemctl resart ssh 


3:Test SSH Key-Based Authentication
At this point, password-based authentication is disabled, and SSH key-based authentication is enabled.
<img width="694" height="380" alt="image" src="https://github.com/user-attachments/assets/c6456d36-9324-43e8-91b0-376ba9dd6612" />

4: hydra brute force test, now that wev'e disabled password authentication we need to 
confirm that the system is resistant to brute-force attacks, we tested it using Hydra with a list of common passwords.
<img width="674" height="484" alt="image" src="https://github.com/user-attachments/assets/74f77a46-a8b1-47d5-8e7d-92f9e2834d1a" />

WHAT I LEARNED 
how to improve server security using KEY_BASED_AUTHENTICATION 
how to protect servers against brute force attacks 
how to analalyze logs and monitor activities on the ubuntu server
