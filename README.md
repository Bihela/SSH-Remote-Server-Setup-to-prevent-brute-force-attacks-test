# SSH-Remote-Server-Setup-to-prevent-brute-force-attacks-test
https://roadmap.sh/projects/ssh-remote-server-setup

A DigitalOcean Ubuntu Droplet: With its IP address (your_server_ip) and an initial login username (e.g., root or ubuntu - let's call it your_server_user) and its password (for the initial ssh-copy-id step).

2. Generate Two New SSH Key Pairs (on WSL Ubuntu)
We'll create two distinct SSH key pairs.
![capture](https://github.com/user-attachments/assets/c95b3ff7-a8b0-460e-a52c-117fce003594)
![Capture1](https://github.com/user-attachments/assets/99fe8841-6e49-423a-a040-e9f2cfb15d24)


3. Add SSH Public Keys to DigitalOcean Server and log in to the server
![Capture2](https://github.com/user-attachments/assets/1ee46191-442e-45aa-9080-7dca276d6a6f)
![Capture4](https://github.com/user-attachments/assets/71513fc9-0736-4d09-be3a-8c0d97333c13)


If successful, you will be logged into your DigitalOcean server.


4. Install fail2ban

![Capture3](https://github.com/user-attachments/assets/b7a16f84-58c0-4344-81a0-0e29325178ff)



Create jail.local configuration file:
It's crucial to NOT edit /etc/fail2ban/jail.conf directly. Instead, create a .local file, which will override the default settings and preserve your configurations during package updates.

sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local

Edit jail.local:

