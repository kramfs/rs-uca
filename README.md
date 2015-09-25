# rs-uca
Rightscale Universal Cloud Appliance

Requirements
-------------
- CentOS 7
- ssh access with root or sudo permission

Clone
-------------
`git clone https://github.com/kramfs/rs-uca.git`

Customize the required inputs
-------------
`cd rs-uca`

`vi setup-uca`

Edit the following adding the required inputs. 
> token="xxyyzz-jf7XuZmSaRSVq8Y5fJ7k"

> api_hostname="us-3.rightscale.com"

> api_credential="n00bsc1yybrt9a45e33ddzz05bobo088300126e22bf"

For the **token**, use something secret i.e TOKEN=`temp_jwG2gkEthvMkYO31VbFw=$`
Use https://www.random.org/strings/?num=1&len=20&digits=on&upperalpha=on&loweralpha=on&unique=on&format=html&rnd=new to generate 20 random string which you can use for the token.

For **api_hostname**, use the shard where the account is located, us-3 or us-4.rightscale.com

As for the **api_credential**, you can get this infomration from the dashboard: *Settings > Account Settings > API Credentials*

Make the file executable:

`chmod +x setup-uca`


Start the script
-------------
This will setup the config file and make the service auto-start on boot

`sudo ./setup-uca`

Next Step:
-------------

Register the UCA Cloud in the RightScale platform - http://uca.surge.sh/uca/reference/register_uca.html

Import ST - https://www.rightscale.com/library/server_templates/RightLink-10/lineage/55642

Enable instance - http://uca.surge.sh/uca/reference/test_uca.html
