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

# CosmosScope<sup>TM</sup> #

To run CosmosScope<sup>TM</sup> installation program, see Running Linux® ELF Binaries in [Common Hint](HintCommon.md).

# HSPICE® #

To run HSPICE®, Intel® Pentium® 4 processor or above compatible processors are required.

An environment variable `CDSB_UNAME_M` has been set as `i386`. If HSPICE not installed, this environment variable should be unset.

`~/.profile`:

> `unset CDSB_UNAME_M`

`~/.cshrc`:

> `unsetenv CDSB_UNAME_M`

# SpiceExplorer<sup>TM</sup> #

If the Java Runtime Environment<sup>TM</sup> does not run correctly, see Installing Java Runtime Environment in [Common Hint](HintCommon.md).

For example, a Java Runtime Environment installed in `$SW_SX_COMMON/platform/i86_r7/java/jre` directory. If it does not run correctly, type:

> `cd $SW_SX_COMMON/platform/i86_r7/java`

> `mv jre jre_sorry`

> `ln -s` _`path_to_jre`_ `jre`

The _`path_to_jre`_ directory is another Java Runtime Environment installation directory.

# Synopsys® Installer #

Before using the Synopsys® Installer, download and run this [patch](http://cdsb.googlecode.com/files/snps_inst_patch.tar.gz).

For example, the Synopsys Installer has been installed in `/compat/linux/opt/synopsys/installer` directory. Run this patch:

> `# gzip -cd snps_inst_patch.tar.gz | tar xvf -`

> `# ./snps_inst_patch/doPatch`

When this patch prompts user to enter the Synopsys Installer installation directory, enter the Synopsys Installer installation directory:

> `# Please enter Synopsys Installer installation directory: /compat/linux/opt/synopsys/installer`

When finish, this patch prompts:

> `# Finish!`


---


Cadence is a registered trademark of Cadence Design Systems, Inc. in the United
States and/or other jurisdictions.

FreeBSD is a registered trademark of the FreeBSD Foundation.

Intel and Pentium are trademarks or registered trademarks of Intel Corporation
in the U.S. and other countries.

Linux® is the registered trademark of Linus Torvalds in the U.S. and other
countries.

Java and Java Runtime Environment are trademarks or registered trademarks of
Sun Microsystems, Inc. in the United States and other countries.

CosmosScope, HSPICE, SpiceExplorer and Synopsys are trademarks or registered
trademarks of Synopsys, Inc.