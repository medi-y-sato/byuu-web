# fork

## develop

そのまま `make all` してもだめなので、

```sh
brew install cmake emscripten wabt
 or
sudo apt install cmake emscripten wabt
```

してから

```sh
make all debug=true
make package
make app
```

## 出力先

`./higan/out/app`

## パッド系の処理

`./byuu-web/higan/target-web/shell.html` の 2011 行目辺りから始まってる `gamepadButtonKeymaps()` とかをなんかするっぽい
