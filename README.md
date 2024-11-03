# COMPYCLOUD PUBLIC IP ASN BLOCK

We collect a large number of IP numbers every year that violate our rules.

If you ISP provider would like to remove your IP number from the list, use Issues or email us at support at compycloud.com.

We welcome suggestions and requests for improvements.

## How do I use your list in my organization?
Use ASNCOMBINED.txt
```yaml
https://raw.githubusercontent.com/Compycloud/ASN_Block/master/ASNCOMBINED.txt
```
And sync this file every hour.

## pfBlockerNG
1. In your pfSense dashboard go to  `Firewall > pfBlockerNG > IP > IP4`
2. Click `Add`
3. Name / Description `CCASN` `COMPYCLOUD ASN Block List`
4. Paste the URL from below
```yaml
IPv4 Source Definitions: Auto ON
```
```yaml
https://raw.githubusercontent.com/Compycloud/ASN_Block/master/ASNCOMBINED.txt
```
```yaml
CCASN_ASNCOMBINED
Action: Deny Both
Update Frequency: Every hour
Weekly (Day of Week): Monday
Auto-Sort Header field: Enable auto-sort
Enable Logging: Enaled
States Removal: Enabled
```
4. Click `Save IPv4 Settings`  
5. Make sure auto updates are on, and you may force update to apply the list immediately. 

## Usage
The list is completely free to use in your own project.
