# Spheron-Network-Worker-Node

Spheron’s Fizz Nodes offer a low-barrier entry point for anyone looking to contribute resources to Spheron’s decentralized compute network—and earn ongoing rewards for their contributions.

Whether you're looking to run a basic CPU configuration or a powerful GPU setup, this guide will walk you through the entire process

***You earn $FN points that will eventually merge with $SPHN tokens***


# Guide to Run Fizz Node

## Hardware Requirement
![373857829-d9d9f0a7-a2f2-41da-8194-16d6dd4b8a00](https://github.com/user-attachments/assets/d6bcdc17-18a5-4305-9f83-19bdf71d998f)


## Register Fizz Node
1. Open Your Browser: Navigate to https://fizz.spheron.network
2. Sign up or log in through Gmail or Github
3. Click on the “Register New Fizz Node” Button and Connect your wallet

![Screenshot 2024-11-13 105817](https://github.com/user-attachments/assets/fdba0eee-a0f9-4b8c-9adf-8203c39bedda)


4. Select your node's OS, resources, Region, Payment Tokens, and Provider ( I linux because i am using a Linux Machine, if you are using personal PC you can choose Windows and also a GPU Node if your pc has a GPU )

![Screenshot 2024-11-13 110634](https://github.com/user-attachments/assets/7fea5805-2caf-4955-ae27-971549f04121)

![Screenshot 2024-11-13 113321](https://github.com/user-attachments/assets/fecd72f9-aca1-41e6-a252-4b2bc2510f37)


5. Click **“Register Your Fizz Node“**, To complete the registration, you'll need some ETH on the Spheron chain for gas fees. If you don't have any, you can get some from our [faucet](https://faucet.spheron.network) or use Arbitrum Sepolia ETH and
[bridge](https://spheron-devnet-eth.bridge.caldera.xyz/) it to the Spheron Chain to complete your registration.



## Run the Fizz Node
1. In setup page for your registered nod, You should find a link to download the `fizzup.sh` script

![Screenshot 2024-11-13 114838](https://github.com/user-attachments/assets/909d658d-7754-4e1a-ae2c-a056c6152a15)


2. Download the `fizzup.sh` script to your PC. Send it to your VPS using `Mobaxterm` or `Termius` Clients

3. Install Docker
```console
sudo apt update -y && sudo apt upgrade -y
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update -y && sudo apt upgrade -y

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo chmod +x /usr/local/bin/docker-compose

# Docker version check
docker --version
```

4. Give persmissions to script
```console
# assuming I transfered the script to the main (root) folder of server
chmod +x /root/fizzup-v1.1.0.sh
```

5. Run Fizz Node Script
```
./fizzup-v1.1.0.sh
```

![image](https://github.com/user-attachments/assets/8c9d5d68-fa8c-42be-96e3-25f9958a0c25)

> You’ll earn more if your node provides higher-tier resources such as a powerful GPU or more CPU cores.

> Fizz Nodes must maintain at least 50% uptime within an ERA (24 hours) to receive rewards

> I've ran this node using CPU-only but you can run with GPU for more rewards

## Check Node health
```
docker compose -f ~/.spheron/fizz/docker-compose.yml logs -f
```
or
```
docker-compose -f ~/.spheron/fizz/docker-compose.yml logs -f
```

![Screenshot 2024-11-13 115517](https://github.com/user-attachments/assets/399e99ba-01d9-4465-8f1f-cd1050aea928)


Once you've verified the node is running, return to the setup page on the Spheron Fizz App

1. On the setup page, you'll see a "Check Status" button and a switch to "Automatically check status." Click the "Check Status" button to manually initiate a status check for your Fizz node

2. Alternatively, you can toggle on the "Automatically check status" switch to have the system periodically check your node's status without manual intervention

![Screenshot 2024-11-13 115627](https://github.com/user-attachments/assets/8e0ad777-aa4a-4737-ac10-4e70a7e24e8a)


3. The system will now perform checks to validate if your node is active and correctly configured

The validation process may take a few minutes. During this time, the system verifies your node's connectivity, resource availability, and configuration. Once your node is confirmed active, you will be automatically directed to your Fizz dashboard

![Screenshot 2024-11-13 115925](https://github.com/user-attachments/assets/f3f727d2-c426-4644-b644-05a8d45baf92)

4. You can now see your phase mutiplier, phase point per era and total phase point

![Screenshot 2024-11-13 120148](https://github.com/user-attachments/assets/7190006a-8067-4eb8-8845-f29e1675003e)

## Claim your NFT in the Dashboard

![Screenshot_371](https://github.com/user-attachments/assets/f4b932eb-1ba4-42aa-837e-8d31b36b67f2)


## Join Discord and Claim your role
Discord: https://discord.gg/spheron-network-745315423783878757

## Connect wallet with OG Nft
Role: https://guild.xyz/spheronfdn

![image](https://github.com/user-attachments/assets/1ffe2ef2-4acc-49df-bc78-b87d7d041f8e)










