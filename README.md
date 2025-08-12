
Установка nix
Включение эксперементальных фичей - в `/etc/nix/conf.nix` прописываю `experimental-features = nix-command flakes`

### Home-manager
https://nix-community.github.io/home-manager/ 
Есть два пути установки home-manager
- standalone 
- NixOS module
Предпочтителен standalone.
https://nix-community.github.io/home-manager/index.xhtml#sec-install-standalone - non-flake
https://nix-community.github.io/home-manager/index.xhtml#sec-flakes-standalone - flake

Выполняю `nix-shell -p home-manager`
Выполняю `home-manager init` - создалить home.nix и flake.nix
Чтобы выполнить rebuild home-manager - `home-manager switch`  или длинный аналог `home-manager switch --flake ~/.config/home-manager/#my-username`

Конфиги для home-manager находятся в `~/.config/home-manager/home.nix` и `~/.config/home-manager/flake.nix`

ПОСЛЕ ПРИМЕНЕНИЯ home-manager - перезапусти терминал, чтобы все точно корректно подхватилось

Чтобы найти больше возможных опций для home-manager - `man home-configuration.nix`

** нужно разобраться как это работает. То есть как он так все обновляет, что у меян все это становится доступно


## Start working

`cd ~/.config`

`git clone git@github.com:ddosmotr/home-manager.git`
