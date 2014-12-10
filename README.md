
							EasyPHY

EasyPHY(tm) Modules allow manufacuturers (OEMs) of BACnet Native controllers to 
decouple their designs from the actual physical network requirements.

The OEM implements a single BACnet protocol layer (BACnet MSTP) on their controller
and this is used to talk to an EasyPHY module.

Then, depending which EasyPHY module is installed, the module simple converts
those BACnet MSTP messages to BACnet/IP, BACnet Ethernet, BACnet over WiFi,
BACnet over Echelon's LIFT, etc.

The simplest EasyPHY module contains just an EIA-485 chip - and this enables a very
cost-effective default of BACnet MSTP, yet allowing the more expensive
other options to be substitued at any time - on the production line or 
in the field!

EasyPHY solutions come as plug-in daughteboards, or wire in (EIA-485 or
logic-level) modules, or as preprogrammed chipsets for on-the-board
assembly, with unique serial numbers, OUIs etc.

ConnectEx, Inc. supplies the modules, and to enhance adoption, free 
hardware reference designs and free reference software, based on the very
well established and popular open source stack by Steve Karg.

Contact info@connect-ex.com for more information.


BACnet-RaspBerryPi-PiFace
=========================

Reference source code for using EasyPHY interfaces on Raspberry Pi platform.

Based on the very popular open-source stack by Steve Karg at https://sourceforge.net/projects/bacnet/?source=directory 


Original "readme.txt"

BACnet open source protocol stack for embedded systems, Linux, and Windows
http://bacnet.sourceforge.net/

Welcome to the wonderful world of BACnet and true device interoperability!

About this Project
------------------

This BACnet library provides a BACnet application layer, network layer and
media access (MAC) layer communications services for an embedded system.

BACnet - A Data Communication Protocol for Building Automation and Control
Networks - see bacnet.org. BACnet is a standard data communication protocol for
Building Automation and Control Networks. BACnet is an open protocol, which
means anyone can contribute to the standard, and anyone may use it. The only
caveat is that the BACnet standard document itself is copyrighted by ASHRAE,
and they sell the document to help defray costs of developing and maintaining
the standard (just like IEEE or ANSI or ISO).

For software developers, the BACnet protocol is a standard way to send and
receive messages on the wire containing data that is understood by other BACnet
compliant devices. The BACnet standard defines a standard way to communicate
over various wires, known as Data Link/Physical Layers: Ethernet, EIA-485,
EIA-232, ARCNET, and LonTalk. The BACnet standard also defines a standard way
to communicate using UDP, IP and HTTP (Web Services).

This BACnet protocol stack implementation is specifically designed for the
embedded BACnet appliance, using a GPL with exception license (like eCos),
which means that any changes to the core code that are distributed get to come
back into the core code, but the BACnet library can be linked to proprietary
code without the proprietary code becoming GPL. Note that some of the source
files are designed as skeleton or example files, and are not copyrighted.

The text of the GPL exception included in each source file is as follows: 

"As a special exception, if other files instantiate templates or use macros or
inline functions from this file, or you compile this file and link it with
other works to produce a work based on this file, this file does not by itself
cause the resulting work to be covered by the GNU General Public License.
However the source code for this file must still be made available in
accordance with section (3) of the GNU General Public License."

The code is written in C for portability, and includes unit tests (PC based
unit tests). Since the code is designed to be portable, it compiles with GCC as
well as other compilers, such as Borland C++ or MicroChip C18.

The BACnet protocol is an ASHRAE/ANSI/ISO standard, so this library adheres to
that standard. BACnet has no royalties or licensing restrictions, and
registration for a BACnet vendor ID is free.

What the code does
------------------

The stack comes with unit tests that can be run in a command shell using the
test.sh script. The unit tests can also be run using individual .mak files.
They were tested on a Linux PC.

The BACnet stack was functionally tested using VTS (Visual Test Shell), another
project hosted on SourceForge, as well as various controllers and workstations.
Using the Makefile in the project root directory, a dozen sample applications
are created that run under Windows or Linux. They use the BACnet/IP datalink
layer for communication by default, but could be compiled to use BACnet 
Ethernet, ARCNET, or MS/TP.


To build and execute on Raspberry Pi platform
---------------------------------------------

$ cd demo/piface
$ ./configure.sh
$ make clean all

