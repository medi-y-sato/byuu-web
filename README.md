# fork

## develop

そのまま `make all` してもだめなので、
<https://emscripten.org/docs/getting_started/downloads.html>
を参考に環境をセットアップする

### mac

```sh
brew install cmake emscripten wabt
```

### Ubuntu/WSL

emscripten はソースインストールした方が間違いがないらしいので、下記のようにする

```sh
sudo apt install cmake wabt

git clone https://github.com/emscripten-core/emsdk.git
git pull
./emsdk install latest
./emsdk activate latest
source ./emsdk_env.sh
```

してから

```sh
make all debug=true
make package
make app
```

お掃除は

```sh
make clean
```

## 出力先

`./higan/out/app`

## パッド系の処理

`./byuu-web/higan/target-web/shell.html` の 2011 行目辺りから始まってる `gamepadButtonKeymaps()` とかをなんかするっぽい
