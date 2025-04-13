# Aesir-1

![Build](https://github.com/OnyxJeff/Aesir-1/actions/workflows/build.yml/badge.svg)
![Maintained](https://img.shields.io/badge/maintained-yes-blue)

**Aesir-1** is my homelab's command center—an Intel NUC running **Proxmox**, managing my container infrastructure via **Portainer**. It powers essential services like:

- `*-darr stack` (Sonarr, Radarr, etc.)
- `netboot.xyz` for PXE booting
- `nginx-proxy-manager` for reverse proxy and SSL management
- `portainer` (because why not manage the manager)

---

## 🚀 Deployment

To deploy a stack:

```bash
cd docker/<stack-name>
docker-compose up -d
```
## 📂 Services
| Stack               | Description                                |
| :---                | :---:                                      |
| darr-stack          | Media automation with Sonarr, Radarr, etc. |
| nginx-proxy-manager |	Reverse proxy with SSL & GUI               |
| netbootxyz          | PXE boot server                            |
| portainer	          | Docker container manager                   |

---

## 💾 Backup
To backup container volumes:

```bash
bash scripts/backup.sh
```
This will tarball volumes for media apps, proxy configs, and Portainer data.

---

📬 Maintained By
Jeff M. • [@OnyxJeff](https://github.com/onyxjeff)