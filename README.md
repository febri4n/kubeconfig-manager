# Kubeconfig Manager

Tool sederhana untuk switching kubeconfig dengan mudah menggunakan fuzzy finder.

## Kenapa ada tool ini?

Kalau kamu sering kerja dengan multiple Kubernetes cluster, pasti familiar dengan ribet-nya ganti-ganti kubeconfig. Tool ini dibuat untuk menyelesaikan masalah itu - cukup ketik `kube` dan pilih config yang mau dipakai.

## Yang dibutuhkan

- `fzf` - buat fuzzy finder interface
- `bash` - udah pasti ada di Unix-like systems

Install fzf:
```bash
# macOS
brew install fzf

# Ubuntu/Debian
sudo apt install fzf

# Arch Linux
sudo pacman -S fzf
```

## Setup

1. Download atau clone repo ini
2. Jadikan executable:
   ```bash
   chmod +x kube
   ```

3. Pindah ke PATH:
   ```bash
   sudo mv kube /usr/local/bin/
   ```

4. Buat folder untuk nyimpan config files:
   ```bash
   mkdir -p ~/.kube/config-file
   ```

5. Pindahin semua kubeconfig ke folder tersebut:
   ```bash
   cp your-kubeconfig-files ~/.kube/config-file/
   ```

## Cara pakai

Tinggal ketik di terminal:
```bash
kube
```

Nanti akan muncul list config yang tersedia, pilih yang mau dipakai dengan arrow keys atau ketik untuk search, tekan Enter untuk konfirmasi.

## Struktur folder

```
~/.kube/
├── config              # current active kubeconfig
└── config-file/        # tempat nyimpan semua kubeconfig
    ├── prod-cluster
    ├── staging-cluster
    └── dev-cluster
```

## Troubleshooting

**Error "fzf: command not found"**
- Install fzf sesuai OS kamu

**Tidak ada config yang muncul**
- Pastikan file kubeconfig ada di `~/.kube/config-file/`
- Check permission file bisa di-read

**Permission denied**
- Pastikan script sudah executable: `chmod +x kube`

## Contributing

Pull request welcome! Kalau ada bug atau feature request, silakan buat issue.

## License

MIT License - bebas dipakai dan dimodifikasi.
