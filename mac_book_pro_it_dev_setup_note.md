# 🧑‍💻 MACBOOK PRO – IT DEV SETUP NOTE

Tài liệu ghi chú nhanh các **phần mềm & công cụ cần cài cho dân IT trên macOS**, kèm **cách cài đặt chuẩn**.

---

## 1️⃣ Công cụ nền tảng (BẮT BUỘC)

### 🔹 Homebrew (Package Manager)
> Quản lý & cài đặt hầu hết tool cho macOS

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Kiểm tra:
```bash
brew --version
```

---

### 🔹 Xcode Command Line Tools
> Cần cho Git, compiler, npm, cocoapods…

```bash
xcode-select --install
```

---

## 2️⃣ Terminal & Shell

### 🔹 iTerm2 (Terminal nâng cao)
```bash
brew install --cask iterm2
```

### 🔹 Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Plugin nên dùng:
- zsh-autosuggestions
- zsh-syntax-highlighting

---

## 3️⃣ Code Editor / IDE

### 🔹 Visual Studio Code
```bash
brew install --cask visual-studio-code
```

Extension nên cài:
- ESLint
- Prettier
- GitLens
- Tailwind CSS IntelliSense
- Material Icon Theme

---

### 🔹 JetBrains IDE (tuỳ nhu cầu)

| Ngôn ngữ | IDE |
|-------|-----|
| Java | IntelliJ IDEA |
| Web | WebStorm |
| Mobile | Android Studio |

```bash
brew install --cask intellij-idea
brew install --cask webstorm
```

---

## 4️⃣ Git & Source Control

### 🔹 Git
```bash
git --version
```

Nếu chưa có:
```bash
brew install git
```

### 🔹 GitHub Desktop
```bash
brew install --cask github
```

---

## 5️⃣ Môi trường lập trình

### 🔹 Node.js / npm
```bash
brew install node
node -v
npm -v
```

👉 Khuyên dùng nvm:
```bash
brew install nvm
```

---

### 🔹 Python
```bash
brew install python
python3 --version
```

---

### 🔹 Java (Backend)
```bash
brew install openjdk
```

---

### 🔹 Docker
```bash
brew install --cask docker
```
(Mở Docker.app sau khi cài)

---

## 6️⃣ Mobile Development

### 🔹 Android Studio
```bash
brew install --cask android-studio
```

### 🔹 CocoaPods (iOS)
```bash
sudo gem install cocoapods
```

---

## 7️⃣ Database & API Tools

### 🔹 Postman
```bash
brew install --cask postman
```

### 🔹 DBeaver (DB Client)
```bash
brew install --cask dbeaver-community
```

---

## 8️⃣ Công cụ hỗ trợ làm việc

### 🔹 Raycast (Launcher)
```bash
brew install --cask raycast
```

### 🔹 Rectangle (Chia màn hình)
```bash
brew install --cask rectangle
```

### 🔹 Notion
```bash
brew install --cask notion
```

---

## 9️⃣ Trình duyệt cho Dev

```bash
brew install --cask google-chrome
brew install --cask firefox
brew install --cask microsoft-edge
```

---

## 🔟 Bảo mật & Tiện ích

### 🔹 1Password
```bash
brew install --cask 1password
```

---

## ⚡ Cài nhanh gợi ý (Basic Dev)

```bash
brew install git node python docker
brew install --cask iterm2 visual-studio-code postman rectangle raycast
```

---

📌 **Ghi chú cá nhân:**
- _______________________________________
- _______________________________________
- _______________________________________

