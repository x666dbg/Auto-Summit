# Autosummit – Roblox Executor Script

> GUI hub + auto-teleport “summit routes” for several mountain games on Roblox. Includes QoL toggles (God Mode, Infinite Jump, Auto Heal), click-to-teleport, and a WalkSpeed slider.

---

## ✨ Fitur Utama

- **Rayfield UI**  
  Panel “Main” & “Auto Summit” dengan toggle/slider yang rapi.

- **Quality of Life**
  - **Infinite Jump** – loncat tanpa batas.
  - **Auto Heal** – pulihkan HP secara bertahap saat kurang dari MaxHealth.
  - **God Mode** – “membekukan” Health agar tidak mati (rename Humanoid → `GodHumanoid` & restore saat < 1).
  - **WalkSpeed Slider** – atur kecepatan jalan.

- **Teleport Tools**
  - **Click Teleport** – equip tool, klik untuk pindah ke `mouse.Hit`.

- **Auto Summit (Route Teleport)**
  - Paket rute (array `CFrame`) untuk berbagai map/gunung:
    - **Yahayuk**
    - **CKPTW**
    - **ATIN**
    - **Merapi (Relog)**
    - **Rinjani**
    - **Hilih**
  - Mesin eksekusi **tahan banting**: `runOnceResilient` memastikan HRP ada, retry set CFrame, jeda antar titik, lalu **auto-reset** karakter saat selesai.

---

## 🗺️ Rute yang Disertakan

Setiap rute adalah **array `CFrame`** yang sudah diurutkan. Script akan:
1. Teleport ke titik `i`.
2. Menunggu jeda (`WAIT_SEC`, default **5 detik**).
3. Lanjut ke titik berikutnya hingga selesai.
4. `resetCharacter()` untuk respawn.

Daftar rute yang tersedia di Tab **Auto Summit**:
- **Auto Summit Gunung Yahayuk**
- **Auto Summit Gunung CKPTW**
- **Auto Summit Gunung ATIN**
- **Auto Summit Gunung Merapi (Relog)**
- **Auto Summit Gunung Rinjani**
- **Auto Summit Gunung Hilih**

Anda bisa menambah rute sendiri—lihat contoh struktur tabel `CFrame` pada script dan panggil `runOnceResilient(<arrayAnda>, <toggleRef>)`.

---

## ⚠️ Disclaimer

- **Gunakan pada risiko Anda sendiri.** Teleport/GodMode dapat terdeteksi oleh anti-cheat; gunakan akun alternatif bila perlu.
- Script ini untuk keperluan edukasi dan modding pribadi; hormati ToS Roblox dan developer game terkait.

---

## 🏁 Quick Loader (contoh)

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/x666dbg/Auto-Summit/refs/heads/main/main.lua", true))()
```
