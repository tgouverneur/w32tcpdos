w32tcpdos.c -- Win32 TCP DoS attack
===================================

coded from Dejan Levaja (dejan_at_levaja.com) advisory
ip/tcp functions ripped from Thamer Al-Herbish.

this easy DoS send a tcp packet with ip.src  == ip.dst,
tcp.src == tcp.dst and
SYN flag set.

Added: sendind many packet at once..

compilation: gcc -Wall -o w32tcpdos2 w32tcpdos2.c

usage:       ./w32tcpdos2 10.59.13.6 135
port can be anything you want, but should be
open on target.

effect:      box under XP SP2 will freeze about 20sec if
their firewall are disabled (windows firewall)

tested against:

- Windows XP SP2 (fw disabled)
- Windows 2k SP4 -> doesn't work.

wildcat -- 2005
<wildcat@espix.org>

