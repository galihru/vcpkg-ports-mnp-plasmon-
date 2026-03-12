# vcpkg Ports for MNP Plasmon

Ports untuk `mnp-plasmon` (C library) dan `mnp-plasmon-cxx` (C++17 library) yang siap didaftarkan ke official vcpkg repository.

## Struktur

```
ports/
├── mnp-plasmon/
│   ├── portfile.cmake      # Build instructions
│   ├── vcpkg.json         # Package metadata
│   └── usage              # Usage documentation
└── mnp-plasmon-cxx/
    ├── portfile.cmake      # Build instructions
    ├── vcpkg.json         # Package metadata
    └── usage              # Usage documentation
```

## Cara Menggunakan Ports Ini

### Manual (untuk testing lokal)

```powershell
# Copy ports ke local vcpkg installation
Copy-Item .\ports\mnp-plasmon -Destination $env:VCPKG_ROOT\ports\
Copy-Item .\ports\mnp-plasmon-cxx -Destination $env:VCPKG_ROOT\ports\

# Install
vcpkg install mnp-plasmon:x64-windows
vcpkg install mnp-plasmon-cxx:x64-windows
```

### Submit ke Official vcpkg

1. Fork: https://github.com/microsoft/vcpkg
2. Clone fork Anda
3. Copy `ports/mnp-plasmon/` dan `ports/mnp-plasmon-cxx/` ke `vcpkg/ports/`
4. Commit dan push
5. Create Pull Request ke microsoft/vcpkg:master

## Paket yang Disediakan

### mnp-plasmon v0.1.0
- C library untuk nanoparticle optical response
- Drude model, Rayleigh polarizability, cross-sections
- Material database (Au, Ag, Al)
- Zero dependencies
- License: GPL-3.0-only

### mnp-plasmon-cxx v0.1.0
- Modern C++17 wrapper
- std::complex support
- Object-oriented API
- Zero dependencies
- License: GPL-3.0-only

## Sumber

- GitHub: https://github.com/galihru/mnpbem
- Repository Physics: Drude model untuk metallic nanoparticles
- Dokumentasi: Lihat linking di usage file

## Status

- [x] Port files created
- [ ] Tested with local vcpkg (optional)
- [ ] PR submitted to microsoft/vcpkg
- [ ] Merged into official vcpkg

---

Generated: March 13, 2026
