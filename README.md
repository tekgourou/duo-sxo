# Duo SecureX Orchestration workflows

Block and activate a Duo user in Cisco SecureX Orchestration


# Prerequisites:

1. Create an Admin API application in Duo and save the credentials.

2. Copy these credentials into Cisco SecureX Orchestration variable section:

- Admin Integration Key (iKey), Host as a string variables [duo_admin_ikey], [duo_host]
- Admin Secret Key (sKey) as a Secure string variable [duo_admin_skey]


3. Create the Duo Target based on the hostname in the Cisco SecureX Orchestration. 

  - Give a name, like "Duo"
  - No account keys: True
  - HTTPS protocol, host/IP address: API hostname
  - Proxy: Ignore Proxy
  
4. Use this "Duo" target in the workflows selecting "Override workflow target" option and "Duo" target.


# Import these workflows into SecureX Orchestration as atomic workflows:

# 1. Duo Admin - Get User.json: 

  This Atomic workflow provides the UserID based on the username.
  
  
# 2. Duo Admin - Block User By UserID.json  

  This Atomic workflow blocks the Duo user based on the UserID.
  
  
# 3. Duo Admin - Activitate User By UserID.json  

  This Atomic workflow activates the Duo user based on the UserID. 


# You can use these workflows:

# 1. Duo Admin - Block User By Username.json  

  This workflow blocks a Duo user based on username. 
  

# 2. Duo Admin - Activate User By Username.json  

  This workflow activates a Duo user based on username. 
  

It was developed based on: https://github.com/SecureX-TME/orchestration/tree/master/atomics created by Matt Vander Horst.
