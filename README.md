# Reboxing Blacklist for bind9 RPZ
### Pointers
As much as possible we do on these below,
  - Free from duplicate domains.
  - Prune sub-domains if domaain present.
  - Throw ip-address in each category (if any) to specific category, [ipv4 category](https://github.com/ngadmini/Reboxing-Blacklist-for-bind9-RPZ/tree/master/ipv4).
  - Remove domains less than 4 characters and larger than 64 characters [RFC 1035](https://www.ietf.org/rfc/rfc1035.txt).
  - Remove domains that construct with international characters (non ASCII).
  - Move (if any) adult, advertise, malware and redirector domains in [trust+](https://raw.githubusercontent.com/alsyundawy/dnstrust-apjii/main/raw/db_trustpositif) to related category. Use domains in [shallalist](https://github.com/cbuijs/shallalist/raw/master/porn/domains.original) for moving identical domains in [trust+](https://raw.githubusercontent.com/alsyundawy/dnstrust-apjii/main/raw/db_trustpositif) TO [db.adult*](https://github.com/ngadmini/Repacking-Blacklist-for-Bind9-rpz/tree/master/adult)
  - Add [gambling](https://dsi.ut-capitole.fr/blacklists/download/gambling.tar.gz) and [gamble](https://github.com/cbuijs/shallalist/raw/master/gamble/domains.original) domains list to [trust+](https://raw.githubusercontent.com/alsyundawy/dnstrust-apjii/main/raw/db_trustpositif).
  - Fixing [TLD](http://data.iana.org/TLD/tlds-alpha-by-domain.txt) typo in [trust+](https://raw.githubusercontent.com/alsyundawy/dnstrust-apjii/main/raw/db_trustpositif) and _false-negative_ in all category.
  - Adult category splitted to variouse _sub-category_ to reduce zones loading
### Original sources blacklist
##### 1. Adult Category -- _[db.adult*](https://github.com/ngadmini/Repacking-Blacklist-for-Bind9-rpz/tree/master/adult)_
Contain adult-porn domains grabbing from sources below,
- [x] https://dsi.ut-capitole.fr/blacklists/download/adult.tar.gz
- [x] https://blocklistproject.github.io/Lists/alt-version/porn-nl.txt
- [x] https://raw.githubusercontent.com/alsyundawy/dnstrust-apjii/main/raw/db_trustpositif
##### 2. ipv4 Category -- _[db.ipv4](https://github.com/ngadmini/Repacking-Blacklist-for-Bind9-rpz/tree/master/ipv4)_
Contain _ip-address_ taken from other category, and grabbing from sources below,
- [x] https://github.com/cbuijs/shallalist/raw/master/porn/domains.original
- [x] https://raw.githubusercontent.com/firehol/blocklist-ipsets/master/firehol_level3.netset
- [x] https://raw.githubusercontent.com/blocklistproject/Lists/master/malware.ip
##### 3. Malware Category -- _[db.malware](https://github.com/ngadmini/Repacking-Blacklist-for-Bind9-rpz/tree/master/malware)_
Contain _malware, ransomware and phishing_ domains grabbing from sources below,
- [x] https://dsi.ut-capitole.fr/blacklists/download/phishing.tar.gz
- [x] https://github.com/cbuijs/shallalist/raw/master/spyware/domains.original
- [x] https://malc0de.com/bl/ZONES
- [x] https://urlhaus.abuse.ch/downloads/rpz
- [x] https://v.firebog.net/hosts/Prigent-Malware.txt
- [x] https://blocklistproject.github.io/Lists/alt-version/phishing-nl.txt
- [x] https://blocklistproject.github.io/Lists/alt-version/malware-nl.txt
- [x] https://blocklistproject.github.io/Lists/alt-version/ransomware-nl.txt
##### 4. Publicite Category -- _[db.publicite](https://github.com/ngadmini/Repacking-Blacklist-for-Bind9-rpz/tree/master/publicite)_
Contain advertishment domains grabbing from sources below,
- [x] https://dsi.ut-capitole.fr/blacklists/download/publicite.tar.gz
- [x] https://github.com/cbuijs/shallalist/raw/master/adv/domains.original
- [x] https://pgl.yoyo.org/adservers/serverlist.php?hostformat=nohtml
- [x] https://v.firebog.net/hosts/Easylist.txt
- [x] https://v.firebog.net/hosts/AdguardDNS.txt
- [x] https://s3.amazonaws.com/lists.disconnect.me/simple_ad.txt 
##### 5. Redirector Category -- _[db.redirector](https://github.com/ngadmini/Repacking-Blacklist-for-Bind9-rpz/tree/master/redirector)_
Contain _vpn, redirector and proxy_ domains grabbing from sources below,
- [x] https://dsi.ut-capitole.fr/blacklists/download/redirector.tar.gz
- [x] https://dsi.ut-capitole.fr/blacklists/download/vpn.tar.gz
- [x] https://github.com/cbuijs/shallalist/raw/master/redirector/domains.original
##### 6. Trust+ Category -- _[db.trust+](https://github.com/ngadmini/Repacking-Blacklist-for-Bind9-rpz/tree/master/trust%2B)_
Based on [trust+](https://raw.githubusercontent.com/alsyundawy/dnstrust-apjii/main/raw/db_trustpositif) BUT reduce from _adult-porn domains_ AND enriched with _gambling domains_ grabbing from sources below,
- [x] https://dsi.ut-capitole.fr/blacklists/download/gambling.tar.gz
- [x] https://github.com/cbuijs/shallalist/raw/master/gamble/domains.original
### Others
##### Credits to
All Owner-Maintener of sources-list (on urls) above
##### License
You can redistribute it and/or modify it under the terms of the **GNU General Public License v3.0**, in the hope that it will be useful.
##### Disclaimer
These script are as they are, and to be used at your own risk
##### Issue and bugs
Please write on [Issue](https://github.com/ngadmini/Reboxing-Blacklist-for-bind9-RPZ/issues) or [Discussions](https://github.com/ngadmini/Reboxing-Blacklist-for-bind9-RPZ/discussions) for questions, feedback and bug fixes
