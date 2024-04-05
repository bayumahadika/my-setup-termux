# MY TERMUX SETUP

[Termux](https://www.termux.dev/en/) adalah salah satu aplikasi alternatif bagi kita yang tidak memiliki komputer/laptop namun ingin mempelajari atau mengembangkan skill pemrograman.

## Download & Instal [Termux](https://www.termux.dev/en/)

[![Download di Github](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/termux/termux-app#github)
[![Download di F Droid](https://img.shields.io/badge/F_Droid-1976D2?style=for-the-badge&logo=f-droid&logoColor=white)](https://f-droid.org/en/packages/com.termux/)

**Download cepat:** [Termux github(v0.118.0 Universal)](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk)

[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://www.youtube.com/@bayumahadika)

---

&nbsp;

## Packages

### Update packages

```sh
pkg update -y && pkg upgrade
```

### Repository & Mirror

```sh
termux-change-repo
```

### Akses Storage

```sh
termux-setup-storage
```

### Install packages

#### Install [NodeJS](https://nodejs.org/en/download/package-manager#android)

```sh
pkg install nodejs -y
```

#### Install [Yarn](https://classic.yarnpkg.com/lang/en/docs/install/#debian-stable)

```sh
pkg install yarn -y
```

#### Install [PHP](https://www.php.net/manual/en/install.php)

```sh
pkg install php -y
```

#### Install [Composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-macos)

```sh
pkg install composer -y
```

#### Install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

```sh
pkg install git -y
```

#### Install [Vim](https://www.vim.org/download.php)

Baca juga: [MY VIM SETUP](https://github.com/bayumahadika/my-vim-setup)

```sh
pkg install vim -y
```

#### Install [Cloudflared](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/get-started/)

```sh
pkg install cloudflared -y
```

#### Install curl

```sh
pkg install curl -y
```

#### Install wget

```sh
pkg install wget -y
```

#### Install [ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)

```sh
pkg install zsh -y
```

#### Perintah singkat(Install semua package)

Perintah singkat untuk mempercepat proses installasi, menginstall semua package diatas:

```sh
pkg install nodejs yarn php composer git vim cloudflared curl wget zsh -y
```

---

## Extra

Merubah default shell dan tampilan Termux

### Download & Install [Termux Styling](https://f-droid.org/id/packages/com.termux.styling/)

Download cepat: [Termux Styling v0.31](https://f-droid.org/repo/com.termux.styling_31.apk)

### Install [Oh My Zsh](https://ohmyz.sh/#install)

#### Menginstall [Oh My Zsh](https://ohmyz.sh/#install) menggunakan curl

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### Menginstall [Oh My Zsh](https://ohmyz.sh/#install) menggunakan wget

```sh
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

### Merubah [Tema Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

Saya menggunakan tema [Refined](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#refined)
Jika anda ingin mencari referensi tema yang cocok dengan anda, anda bisa langsung mengunjungi [Themes Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

Setelah menemukan Tema yang cocok, sekarang kita perlu menerapkannya.
Gunakan perintah sebagai berikut (Sesuaikan nilai ZSH_THEME="refined" dengan tema yang anda inginkan):

```sh
sed -i 's/ZSH_THEME="robbyrussell"/ZSH_THEME="refined"/' ~/.zshrc && source ~/.zshrc
```

### Install Plugins [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins)

Apabila kita menginstall [Oh My Zsh](https://ohmyz.sh/) hanya merubah tema saja, tidak menambahkan plugins tambahan yang disediakan oleh [Oh My Zsh](https://ohmyz.sg/) sepertinya kurang.

Kita bisa menambahkan beberapa plugins, untuk mempermudah pekerjaan kita sehari-hari.

#### My Plugins Oh My Zsh

> **Plugins yang saya gunakan:**
>
> - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
> - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
> - [fast-syntax-highlighting](https://github.com/zdharma-continuum/fast-syntax-highlighting)
> - [zsh-autocomplete](https://github.com/marlonrichert/zsh-autocomplete)

Referensi Plugin ? [Plugins Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins)

#### Install Plugin [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

#### Install Plugin [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)

```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

#### Install Plugin [fast-syntax-highlighting](https://github.com/zdharma-continuum/fast-syntax-highlighting#installation)

```sh
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git \
  ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting
```

#### Install Plugin [zsh-autocomplete](https://github.com/marlonrichert/zsh-autocomplete#installing--updating)

```sh
git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete
```

##### Penerapan Plugin

Setelah proses instalasi selesai, langkah selanjutnya kita perlu menerapkan plugin dengan cara mengubah konfigurasi Zsh untuk memasukkan plugin yang diinginkan ke dalam file `~/.zshrc`.

1. Edit file `~/.zshrc`

```sh
nano ~/.zshrc
```

2. Cari bagian konfigurasi plugins

```sh
plugins=(git)
```

Tambahkan nama plugin yang sudah anda install sebelumnya.
Berhubung saya menginstall beberapa plugins [ini](https://github.com/bayumahadika/my-termux-setup#my-plugins-oh-my-zsh), Jadi saya perlu mengubahnya seperti ini:

```sh
plugins=(git zsh-autosuggestions zsh-syntax-highlighting fast-syntax-highlighting zsh-autocomplete)
```

3. Simpan perubahan file
   Tekan `ctrl+x`, `Y`, `enter`.
4. Memuat ulang konfigurasi

```sh
source ~/.zshrc
```

> Alternatife atau cara cepat menerapkan plugin dan memuat ulang konfigurasi:
>
> `sed -i 's/plugins=(git)/plugins=(git zsh-autosuggestions zsh-syntax-highlighting fast-syntax-highlighting zsh-autocomplete)/' ~/.zshrc && source ~/.zshrc`

---

&nbsp;

### Sosial Media

[![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white)](https://www.facebook.com/bayumahadika7)

[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white)](https://www.instagram.com/bayu.mahadika)

[![TikTok](https://img.shields.io/badge/TikTok-%23000000.svg?style=for-the-badge&logo=TikTok&logoColor=white)](https://www.tiktok.com/@bayu.mahadika)

[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://youtube.com/@bayumahadika)

---

&nbsp;
