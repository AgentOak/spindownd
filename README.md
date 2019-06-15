## spindownd

Daemon to spin down active hard disks after a period of inactivity.

Features a spindown limit to prevent excessive wear on the disks.

### Requirements

* `/usr/sbin/smartctl`
* `/sbin/hdparm`
* php, 7.1+

### Usage

Run `./spindownd --help`.

### Run as a service

It is recommended to run spindownd as a systemd service.
An example service unit file has been included in `spindownd.service`.
Place this file in `/etc/systemd/system/` and modify it to your needs.
To enable the service run `systemctl enable spindownd`, to start it `systemctl start spindownd`.
Check logs using `journalctl -u spindownd` (See journalctl manual for more options).

### License

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
