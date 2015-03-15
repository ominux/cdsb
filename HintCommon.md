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

# Installing Ports Tree #

Install or update the Ports tree.

For example, use the `portsnap` command.

Install the Ports tree:

> `portsnap fetch extract`

Update the Ports tree:

> `portsnap fetch update`

# Running CDSB #

Download and run [CDSB](http://cdsb.googlecode.com/files/cdsb_1.1.1.tar.gz).

See CdsbReadMe for details.

# Using RC Script #

If the rc script is needed. Put it in the `/compat/linux/etc/rcCDS.d` directory.

The `/compat/linux/etc/rcCDS.d` directory contains rc scripts of Cadence® products. File names in `/compat/linux/etc/rcCDS.d` are of the form `S??*` or the form `K??*` where `S` means start this script, `K` means kill this script, and `??` is the relative sequence number for starting or killing the script.

At system boot, the `/usr/local/etc/rc.d/cdsrc` script executes those scripts in `/compat/linux/etc/rcCDS.d` that are prefixed with `S`. At system shutdown, the `/usr/local/etc/rc.d/cdsrc` script executes those scripts in `/compat/linux/etc/rcCDS.d` that are prefixed with `K`.

When executing each script in `/compat/linux/etc/rcCDS.d`, the `/usr/local/etc/rc.d/cdsrc` script passes a single argument. It passes the argument `start` for scripts prefixed with `S` and the argument `stop` for scripts prefixed with `K`.

# Installing Java Runtime Environment<sup>TM</sup> #

If the Java Runtime Environment<sup>TM</sup> for Linux® does not run correctly on FreeBSD, install the other version of the Java Runtime Environment from Ports, then create a link to point to it.

# Using Linux Shell #

Create an account, this account use a Linux shell, such as `/compat/linux/bin/sh` or `/compat/linux/bin/csh`.

If use the C shell, `/compat/linux/bin/csh` and `/compat/linux/bin/tcsh`, in order to locate the root directory correctly, add following to `~/.cshrc` or `~/.tcshrc`:

```
 set path=( $path \
            /../sbin \
            /../bin \
            /../usr/sbin \
            /../usr/bin \
            /../usr/games \
            /../usr/local/sbin \
            /../usr/local/bin \
            /../usr/X11R6/bin \
          )
```

For example, use the `adduser` command to create an account, the user name is `edauser`.

# Setting Environment Variables #

If the login shell is a Linux shell, the environment variable LIBXCB\_ALLOW\_SLOPPY\_LOCK will be set as `1` when user login.

If the login shell is not a Linux shell, the environment variable LIBXCB\_ALLOW\_SLOPPY\_LOCK must be set as `1` by user.

`~/.profile`:

> `LIBXCB_ALLOW_SLOPPY_LOCK='1'; export LIBXCB_ALLOW_SLOPPY_LOCK`

`~/.cshrc`:

> `setenv LIBXCB_ALLOW_SLOPPY_LOCK '1'`

# Running Linux ELF Binaries #

If a Linux Binaries does not run, type:

> `brandelf -t Linux` _`linux_elf_binary`_

_`linux_elf_binary`_ is a Linux binary.


---


Cadence is a registered trademark of Cadence Design Systems, Inc. in the United
States and/or other jurisdictions.

FreeBSD is a registered trademark of the FreeBSD Foundation.

Linux® is the registered trademark of Linus Torvalds in the U.S. and other
countries.

Java and Java Runtime Environment are trademarks or registered trademarks of
Sun Microsystems, Inc. in the United States and other countries.