# Quantis
Shell script to install a [Quantis Masternode](http://quantis.network/) on a Linux server running Ubuntu 16.04.  
This script will install **quantis v1.0**.
***

## Installation:
```
wget -q https://raw.githubusercontent.com/Realbityoda/quantis/master/quantis_install.sh
bash quantis_install.sh
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open the quantis Core Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **50000** **quantis** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  ** Tools -> "Open Masternode Configuration File"
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6** 
* Output index:  **Second value from Step 6** It can be **0** or **1**
9. Click OK and exit the Wallet.
10. Open quantis Core Wallet, go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again.
10. Click **Start All** or **Start Alias**
11. If you are not able to see your **Masternode**, try to close and open your desktop wallet.
***

## Usage:
```
quantisd getinfo
quantisd masternode status
quantisd mnsync status
```
Also, if you want to check/start/stop **quantis** , run one of the following commands as **root**:
```
systemctl status quantisd #To check the service is running.
systemctl start quantisd #To start quantis service.
systemctl stop quantisd #To stop quantis service.
systemctl is-enabled quantisd #To check whetether quantis service is enabled on boot or not.
```


## Donations:  

Any donation is highly appreciated.  

**QUAN**:  TT9XTjHzs74F5ZwBovXtVyotRRMmBynfga  
**BCH**: qzgnck23pwfag8ucz2f0vf0j5skshtuql5hmwwjhds  
**ETH**: 0x765eA1753A1eB7b12500499405e811f4d5164554  
**LTC**: LNt9EQputZK8djTSZyR3jE72o7NXNrb4aB
