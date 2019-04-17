# GY7 
## zh
> A zh csak a 4. beadandóig lesz számonkérve, csak socket programozás. udp lehet! 4esért ötösért már háromszereplős rész
## mininet
- `pingall` minden hoszt mindenkit pingel
- `ip` cím és `netmask` páros ip alhálózatot - `subnetet` ír le, ha az ipt és a netmaskot binárisba váltjuk át és összeéseljük akkor megkapjuk a subnetet.
- ip routing tábla: `ip ro sh` vagy `ip route show` ha egyik tartományba küldünk akkor egyfele megy ki a csomag.

## routing tábla
- routing tábla bvejegyzésén az az alhálózat van amire egyeznie kell a hálózatnak és mire küldi ki, a routing tábla a legkisebb szabályok közül a legelsőt használja
- szabályokat adhatunk meg: `ip ro add 10.0.10.0/24 dev h2-eth0`szabályokat törölhetünk is `del`lel `add` helyett.
- linuxban beállítható hogy kapjuk el a nem nekünk szóló csomagokat is   `echo 1> /proc/sys/net./ipv4/ip_forwardes`

## konfigurálás
- `ifconfig h2-eth0`
- `iptables`
- `ip_forward`
- `ipstables-save`

- loopback forgalom ok
- én kifele ok
- multicast csomagokat eldobom
- minden egyéb input drop
