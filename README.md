Bitcoin full-node scripts
=========================

This repository contains Linux scripts to help working with bitcoin tools and full-nodes.

bitcoin-proxy
-------------

Simply routes traffic between two ports. Defaults to bitcoin port 8333.

**Instructions**

  1. Download script
  2. Upload Linux machine
  3. Make it executable with `chmod +x bitcoin-proxy`
  4. (optional) Add script to the `PATH`

**Examples**

`$> ./bitcoin-proxy -h`

Shows help.

`$> ./bitcoin-proxy 10.0.1.32`

Proxy TCP port 8333, on all interfaces, to TCP port 8333 of IP 10.0.1.32

`$> ./bitcoin-proxy -p 18333 -a bch.site.com localhost 8333`

Proxy TCP port 18333, on the interface maching bch.site.com, to TCP port 8333 of the loop back interface.

**Dependency on ncat**

The script depends on the ncat utility. The ncat utility is included with the nmap package.

`apt-get install nmap`

**Caveats**

  * Options are only minimally validated. If an argument is missing or invalid the script may fail silently.
  * Tested in Debian system. May be relevant due to ncat dependency.
