<!-- README.md -->

# <p align="center">kernel-modules-hook</p>

Tired of missing modules when updating the kernel?<br/>
Annoyed by `modprobe: FATAL: Module smth not found in directory /lib/modules/new-kernel`?<br/>
Losing uptime after reboots due to kernel update?

[View on the AUR](https://aur.archlinux.org/packages/kernel-modules-hook/).

*The solution is here.*

* Save.<br/>
![Save](https://i.imgur.com/3YHtBRB.png)<br/>
* Update.<br/>
![Update](https://i.imgur.com/uxySEMY.png)<br/>
* Restore.<br/>
![Restore](https://i.imgur.com/AJeBw0n.png)<br/>
* Enjoy.<br/>
![Enjoy](https://i.imgur.com/WQAYSSR.png)

Do not worry, backups are automatically cleaned.

## Installation

#### From the AUR:
```bash
"$YOUR_FAVORITE_AUR_HELPER" -S kernel-modules-hook
```

#### Or from git:

```bash
git clone https://github.com/saber-nyan/kernel-modules-hook.git
cd kernel-modules-hook
makepkg -sci
```

### Enable automatic cleanup:

```bash
sudo systemctl daemon-reload
sudo systemctl enable linux-modules-cleanup.service
```

<!-- vim: set ts=2 sw=2 et syn=markdown: -->
