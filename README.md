# Wake-on-LAN
Program to remotely Power On a PC over the internet using the Wake-on-LAN protocol

Note : Wake-on-LAN (WoL) is an Ethernet or token ring computer networking standard that allows a computer to be turned on or awakened by a network message.


                                      *********************Magic Packet Structure************************* 
                                      
The magic packet is a broadcast frame containing anywhere within its payload 6 bytes of all 255 (FF FF FF FF FF FF in hexadecimal), followed by sixteen repetitions 
of the target computer’s 48-bit MAC address, for a total of 102 bytes. Since the magic packet is only scanned for the string above, and not actually parsed by a full 
protocol stack, it may be sent as any network- and transport-layer protocol, although it is typically sent as a UDP datagram to port 0, 7, or 9, or directly over Ethernet 
as EtherType 0x0842.


*************************************************A standard magic packet has the following basic limitations************************************************

1. Requires destination computer MAC address (also may require a SecureOn password).
2.Do not provide a delivery confirmation.
3. May not work outside of the local network.
4. Requires hardware support of Wake-On-LAN on the destination computer.
5. Most 802.11 wireless interfaces do not maintain a link in low power states and cannot receive a magic packet.

The Wake-on-LAN implementation is designed to be very simple and to be quickly processed by the circuitry present on the network interface card with minimal power requirement. 
Because Wake-on-LAN operates below the IP protocol layer the MAC address is required and makes IP addresses and DNS names meaningles

OutPut - 
