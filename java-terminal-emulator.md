# Java terminal emulator

## Telnetd
Telnetd seems to be a complete an pretty well documented solution:

http://telnetd.sourceforge.net/

## JCTerm
JCTerm behaves like a VT100 and uses a SSH2 connection. But the website indicates the VT100 emulation is incomplete.

http://www.jcraft.com/jcterm/

## JediTerm
JediTerm has both graphical implementation as well as API to override.
Graphical version works for remote connections(using JSch) and local pty(using JPty).

https://github.com/JetBrains/jediterm