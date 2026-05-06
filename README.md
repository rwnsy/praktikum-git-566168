# Praktikum Git — [566168]

Website komunitas buku yang dibangun sebagai tugas praktikum Git & GitHub.
Proyek ini mencakup halaman utama dengan navbar, hero section, book card,
discussion item, CTA, dan footer.

## Cara Menjalankan

1. Clone repo ini: `git clone https://github.com/rwnsy/praktikum-git-566168`
2. Buka folder: `cd praktikum-git-566168`
3. Buka `index.html` di browser

## Screenshot

![Website](gambar/website.png)

🔧 Dokumentasi Perintah Git
⚙️ Setup & Inisialisasi
Perintah Penjelasan
git init Menginisialisasi repository Git baru di folder lokal
git clone <url> Menyalin repository dari GitHub ke lokal
git config --global user.name "..." Mengatur nama pengguna
git config --global user.email "..." Mengatur email pengguna
📸 Stage & Commit
Perintah Penjelasan
git status Melihat status file
git add . Menambahkan semua perubahan ke staging
git add <file> Menambahkan file tertentu
git commit -m "pesan" Menyimpan perubahan
git log --oneline --graph Melihat riwayat commit secara ringkas
✍️ Contoh Commit

Menggunakan Conventional Commits:

git commit -m "feat: add navbar navigation"
git commit -m "fix: resolve merge conflict"
git commit -m "chore: add gitignore"
git commit -m "docs: add README with git log screenshot"
![git log --oneline --graph](gambar/log.png)

🌿 Branching
Perintah Penjelasan
git branch Melihat daftar branch
git switch -c <branch> Membuat & pindah branch
git switch <branch> Pindah branch
git branch -d <branch> Menghapus branch
git push -u origin <branch> Push branch pertama kali
📌 Branch yang Digunakan
feature/navbar → tambah navbar
feature/footer → tambah footer
hotfix/typo → perbaiki typo
experiment/color-A & experiment/color-B → simulasi konflik

![Branch Protection Rule](gambar/branchpr.png)

🔀 Merge & Konflik
Perintah Penjelasan
git merge <branch> Menggabungkan branch
git merge --no-ff <branch> Merge dengan commit khusus
git status Cek konflik
git add <file> Tandai konflik selesai
git commit Menyelesaikan merge
⚠️ Simulasi Konflik

Konflik terjadi karena:

color-A dan color-B mengubah baris CSS yang sama
Setelah color-A di-merge ke main, merge color-B menimbulkan konflik

📌 Penyelesaian:

Edit manual di VS Code
Hapus tanda konflik (<<<<, ====, >>>>)
git add → git commit
![Konflik](gambar/konflik.png)

♻️ Rebase
Perintah Penjelasan
git rebase main Update base branch
git rebase -i HEAD~3 Interactive rebase
git rebase --continue Lanjut rebase
git rebase --abort Batalkan rebase
✨ Penggunaan
Branch: feature/dark-mode
3 commit digabung (squash) jadi 1 commit:
feat: implement dark mode

- change background to dark
- adjust navbar color
- improve card contrast
  ☁️ Remote & Sinkronisasi
  Perintah Penjelasan
  git remote add origin <url> Hubungkan ke GitHub
  git push origin main Push ke remote
  git pull --rebase Sinkronisasi tanpa merge commit
  git fetch origin Ambil data tanpa merge
  🔒 Branch Protection

Branch main dilindungi dengan aturan:

✅ Wajib Pull Request
✅ Tidak boleh push langsung
✅ Semua perubahan harus melalui review

📸 Screenshot:

![Branch Protection](assets/branch-protection.png)
📌 Issues
Issue Judul Status
#4 Add dark mode feature ✅ Closed
#5 Fix typo pada CTA ✅ Closed
#6 Improve footer information ✅ Closed

Semua issue diselesaikan melalui Pull Request menggunakan:

Closes #nomor
🏷️ Release
🚀 v1.0.0

Rilis pertama project praktikum.

Fitur:

Navbar
Book cards
Discussion section
CTA section
Footer

Teknis:

Implementasi branching
Simulasi konflik & merge
Interactive rebase (squash commit)
Pull Request & Issues workflow
