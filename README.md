# Ips
Shell script to install a [Ips Masternode](https://ipsum.im/) on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## VPS installation
```
wget -q https://raw.githubusercontent.com/PLGCoin/Ips/patch-1/ips_install.sh
bash ips_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Ips Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **5000** Ips to **MN1**. You need to send all 10000 coins in one single transaction.
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to  **Tools -> "Open Masternode Configuration File"**
8. Add the following entry:
```
Alias Address Privkey TxHash TxIndex
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* TxIndex:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
12. Select your MN and click **Start Alias** to start it.
13. Alternatively, open **Debug Console** and type:
```
masternode start-alias MN1
``` 
14. Login to your VPS and check your masternode status by running the following command:.
```
ips-cli masternode status
```
***

## Usage:
```
ips-cli masternode status  
ips-cli getinfo
```
Also, if you want to check/start/stop **Ips**, run one of the following commands as **root**:

```
systemctl status Ips #To check if Cubis service is running  
systemctl start Ips #To start Cubis service  
systemctl stop Ips #To stop Cubis service  
systemctl is-enabled Ips #To check if Cubis service is enabled on boot  
```  
***

## Donations

Any donation is highly appreciated

**BTC**: 3KShHHwv4KJboBAGKQNbQzEhL8uvFcXRwA  
**ETH**: 0x5Ec79a5f8D1aC11a748fC847078249a08b68c38F  
**LTC**: LXWNb37gqpGKT5rLeC8YHirESsrguuY3DU  
**IPS**: idWuCHYNFs2aBCJJhZbqTGp2SmT8TMryRE
