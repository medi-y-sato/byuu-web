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
make all debug=true ; make app ; make serve 
```

リリースは

```sh
make all debug=false ; make package
```

出力先は `./higan/out/app` になる

お掃除は

```sh
make clean
```

開発の時はビルド前必ずcleanしとくべき、わりとビルド済みの誤判定する

```sh
make clean ; make all debug=true ; make app ; make serve
```

## 出力先



## パッド系の処理

`./byuu-web/higan/target-web/shell.html` の 2011 行目辺りから始まってる `gamepadButtonKeymaps()` とかをなんかするっぽい
