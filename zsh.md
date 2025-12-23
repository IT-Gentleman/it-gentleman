# zsh 설정
## Ubuntu
1. 필수 패키지 및 zsh 설치
    ```bash
    sudo apt update
    sudo apt install zsh curl git -y
    chsh -s $(which zsh)
    ```
2. Oh My Zsh 설치 (프레임워크)
    ```bash
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
3. 필수 플러그인 설치
    1. zsh-autosuggestions
        ```bash
       git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
       ```
    2. zsh-syntax-highlighting
       ```bash
       git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
       ```
4. 테마 설치: Powerlevel10k
    - 테마 다운로드
       ```bash
       git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
       ```
    - 권장 폰트 다운로드
       1. 폰트 다운로드
           ```bash
           mkdir -p ~/.local/share/fonts
           cd ~/.local/share/fonts
           wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf
           wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf
           wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf
           wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf
           ```
       2. 폰트 캐시 갱신
           ```bash
           fc-cache -f -v
           ```
6. 설정파일 적용: .zshrc (`nano .zshrc`)
   ```bash
   ZSH_THEME="powerlevel10k/powerlevel10k"
   ```
   ```bash
   plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
   ```
7. 로그아웃 후 다시 로그인


## Mac
### iTerm2 사용
1. iTerm2 설치
    `https://iterm2.com/`
2. Oh My Zsh 설치 (프레임워크)
    ```bash
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
3. 필수 플러그인 설치
    1. zsh-autosuggestions
        ```bash
       git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
       ```
    2. zsh-syntax-highlighting
       ```bash
       git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
       ```
4. 테마 설치: Powerlevel10k
    - 테마 다운로드
       ```bash
       git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
       ```
    - 권장 폰트 다운로드
       iTerm2에서는 자동 다운로드됨
5. 설정파일 적용: .zshrc (`nano .zshrc`)
   ```bash
   ZSH_THEME="powerlevel10k/powerlevel10k"
   ```
   ```bash
   plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
   ```
7. 로그아웃 후 다시 로그인
### 기본 터미널 사용
1. Oh My Zsh 설치 (프레임워크)
    ```bash
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
2. 필수 플러그인 설치
    1. zsh-autosuggestions
        ```bash
       git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
       ```
    2. zsh-syntax-highlighting
       ```bash
       git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
       ```
3. 테마 설치: Powerlevel10k
    - 테마 다운로드
       ```bash
       git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
       ```
    - 권장 폰트 다운로드
       1. 폰트 다운로드
           ```bash
           mkdir -p ~/Downloads/meslo
           cd ~/Downloads/meslo
            
           curl -LO "https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf"
           curl -LO "https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf"
           curl -LO "https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf"
           curl -LO "https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf"
            
           mv *.ttf ~/Library/Fonts/
           ```
       2. 터미널 폰트 변경 (MesloLGS)
4. 설정파일 적용: .zshrc (`nano .zshrc`)
   ```bash
   ZSH_THEME="powerlevel10k/powerlevel10k"
   ```
   ```bash
   plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
   ```
5. 로그아웃 후 다시 로그인
