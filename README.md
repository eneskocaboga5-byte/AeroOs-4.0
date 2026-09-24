# AeroOs 4.0 🚀

AeroOs 4.0 is a lightweight, fast, and independent **rolling-release** operating system distribution built on top of **musl libc**, using **runit** for init and service management, and featuring its own dedicated **apm** (Aero Package Manager) repositories.

⚠️ **PROJECT STATUS: BETA**
AeroOs 4.0 is currently in its **Beta development stage**. While it is functional, some features, core packages, and repository structures are subject to change. It is currently **not recommended for critical production environments**. Testing, feedback, and bug reports are highly welcome!

As a **rolling-release distribution**, AeroOs 4.0 does not require periodic full-system upgrades or re-installations. Once installed, your system receives continuous updates for all software and core components directly from the bleeding-edge `apm` repositories.

This repository serves as the central hub for the official **apm repositories** and package definitions for the AeroOs 4.0 ecosystem.

## 🌟 Key Features

*   **Beta Rolling Release Model:** Continuous updates and bleeding-edge software packaged directly for our testing phase. Install once, update forever.
*   **Musl Libc:** Lightweight, secure, and clean system architecture optimized by utilizing musl instead of standard glibc.
*   **Runit Init & Service Manager:** A minimal, robust, and ultra-fast service architecture replacing systemd for blazing-fast boot times.
*   **APM (Aero Package Manager):** A custom package and repository management system tailored specifically for AeroOs, inspired by the efficiency of `apk`.

## 📦 Repository Structure

Packages in this repository are organized into distinct directories, continuously updated to match the rolling-release lifecycle:

*   `core/`: Critical packages required for system boot and core operations (musl, runit, apm, etc.).
*   `main/`: Stable and thoroughly tested essential tools and applications.
*   `community/`: Additional software maintained and extended by the community.

## 🛠️ APM Usage Guide

Since AeroOs 4.0 is a rolling release, keeping your system updated is crucial. Use the following fundamental `apm` commands:

### Synchronize Repositories & Full System Upgrade
To keep your rolling-release system completely up-to-date, always sync and upgrade:
```bash
apm update && apm upgrade
```

### Search for a Package
```bash
apm search <package-name>
```

### Install a Package
```bash
apm add <package-name>
```

### Remove a Package
```bash
apm del <package-name>
```

## ⚙️ Service Management (Runit)

Service management on AeroOs 4.0 leverages the simple and powerful `runit` command structure:

*   **Enable and start a service:** `ln -s /etc/sv/<service-name> /var/service/`
*   **Check service status:** `sv status <service-name>`
*   **Stop a service:** `sv down <service-name>`
*   **Restart a service:** `sv restart <service-name>`

## 🤝 Contributing & Bug Reporting

Since we are in **Beta**, your contributions are extremely valuable! If you encounter any bugs or want to add/update a package:

1. Fork this repository.
2. Open an issue describing the bug, or create a feature branch for your package (`git checkout -b feature/update-package`).
3. Modify or create the package definition file (e.g., `APMBUILD`) in the appropriate directory.
4. Commit your changes (`git commit -m 'Update: <package-name> to X.Y.Z'`).
5. Push to the branch (`git push origin feature/update-package`).
6. Open a Pull Request.

## 📄 License

This project is licensed under the [MIT License](LICENSE).
