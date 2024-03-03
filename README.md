# as2ipset
Creates ipset shell script from an autonomous system (AS) IP addresses from RIPE database.<br />
Supports both of IPv4 and IPv6.<br />
<br />
Usage:  ./as2ipset.py \<ASXXXX\> \<.{/AS_ipvX.ipset}\><br />
<br />
AS_ipv4.ipset:<br />
ipset flush ipv4_AS<br />
ipset x ipv4_AS<br />
ipset n ipv4_AS hash:net hashsize 16384 maxelem 262144<br />
ipset add ipv4_AS A1.B1.C1.D1/E1<br />
ipset add ipv4_AS A2.B2.C2.D2/E2<br />
<br />
AS_ipv6.ipset:<br />
ipset flush ipv6_AS<br />
ipset x ipv6_AS<br />
ipset n ipv6_AS hash:net hashsize 16384 maxelem 262144 family inet6<br />
ipset add ipv6_AS A1::/B1<br />
ipset add ipv6_AS A2::/B2<br />
