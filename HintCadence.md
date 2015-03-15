CDSB - Prepare for Installation of Cadence® products on FreeBSD.

Copyright © 2008 Zhang Liang

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

Email: meitolake@gmail.com

# Creating Managing Account #

Create an account for managing Cadence® software, this account should use the Linux® shell, such as `/compat/linux/bin/sh` or `/compat/linux/bin/csh`.

For example, use the `adduser` command to create an account, the user name is `cdsmgr`.

# Installing Netscape® Web Browser #

Install the [Netscape® web browser](http://browser.netscape.com/releases) 4.x for Linux or later. Such as 7.x.

# Using Cadence® InstallScape<sup>TM</sup> Installation Program #

See Installing Java Runtime Environment<sup>TM</sup> in [Common Hint](HintCommon.md).

The InstallScape<sup>TM</sup> installation program contains the Java Runtime Environment in the `iscape/runtime` directory, named `LNX86`. To create a link, Type:

> `mv LNX86 LNX86_sorry`

> `ln -s` _`path_to_jre`_ `LNX86`

The _`path_to_jre`_ directory is another Java Runtime Environment installation directory.

If the use of installscape encounter any accidents, try using the batch mode.


---


Netscape is a registered trademark of America Online, Inc. in the United States and/or other countries.

Cadence is a registered trademark of Cadence Design Systems, Inc. in the United States and/or other jurisdictions.

FreeBSD is a registered trademark of the FreeBSD Foundation.

Linux® is the registered trademark of Linus Torvalds in the U.S. and other countries.

Java and Java Runtime Environment are trademarks or registered trademarks of Sun Microsystems, Inc. in the United States and other countries.