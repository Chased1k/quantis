# Toba
Shell script to install a [Toba Masternode](http://toba.fun/) on a Linux server running Ubuntu 16.04.  
This script will install **toba v1.0**.
***

## Installation:
```
wget -q https://raw.githubusercontent.com/Realbityoda/toba/master/toba_install.sh
bash toba_install.sh
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open the toba Core Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **50000** **TOBA** to **MN1**.
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
10. Open toba Core Wallet, go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again.
10. Click **Start All** or **Start Alias**
11. If you are not able to see your **Masternode**, try to close and open your desktop wallet.
***

## Usage:
```
tobad getinfo
tobad masternode status
tobad mnsync status
```
Also, if you want to check/start/stop **toba** , run one of the following commands as **root**:
```
systemctl status tobad #To check the service is running.
systemctl start tobad #To start toba service.
systemctl stop tobad #To stop toba service.
systemctl is-enabled tobad #To check whetether toba service is enabled on boot or not.
```


## Donations:  

Any donation is highly appreciated.  

**TOBA**:  TT9XTjHzs74F5ZwBovXtVyotRRMmBynfga  
**BCH**: qzgnck23pwfag8ucz2f0vf0j5skshtuql5hmwwjhds  
**ETH**: 0x765eA1753A1eB7b12500499405e811f4d5164554  
**LTC**: LNt9EQputZK8djTSZyR3jE72o7NXNrb4aB
