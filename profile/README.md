![Atomix Logo](assets/atomix-banner.png)

# 🎮 Atomix Linux

**Atomix Linux** is an immutable, Flatpak-centric Linux distribution for gamers. Built on Fedora Atomic technologies, Atomix provides a stable, minimal base with containerized gaming apps, OSTree updates, and GPU-ready profiles.

---

## 🚀 Key Features

- 🔒 **Immutable base system** via rpm-ostree and OSTree
- 🎮 **Gaming-Ready** out of the box with Steam, Heroic, Lutris and more...
- 📦 **Flatpak-first** approach for all user apps
- 🧱 **Multiple Editions** You can install Atomix Linux in Plasma Edition, Gnome Editon, Steam Deck Plasma Edtion, Steam Deck Gnome Edtion, Plasma NVIDIA edition, Gnome NVIDIA edition, Steam Deck Plasma NVIDIA edition and Steam Deck Gnome NVIDIA edition.
- 📡 **Atomic updates** with system rollback capability

## 📥 Installation Process
> Requirments x86_64 system, 4 GB RAM, 50 GB Space

### By ISO
- Not Ready Yet

### From Existing OSTree based distro installation
- First Command in terminal to rebase image

```bash
rpm-ostree rebase ostree-unverified-registry:ghcr.io/atomix-linux/atomix:latest
```
- You can replace atomix:latest, with atomix-unstable:latest, but its not recommended, you can also use other editions to install Atomix

- Then reboot system

```bash
systemctl reboot
```

- Then rebase the signed image

```bash
rpm-ostree rebase ostree-image-signed:docker://ghcr.io/atomix-linux/atomix:latest
```

- Remember to use the same image as the first command

- Then reboot again and done.

```bash
systemctl reboot
```
