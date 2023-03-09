# fork

## develop

そのまま `make all` してもだめなので、

```sh
brew install cmake
brew install emscripten
brew install wabt
```

してから

```sh
make all debug=true
make package
make app
```

## パッド系の処理

`./byuu-web/higan/target-web/shell.html` の 2011 行目辺りから始まってる `gamepadButtonKeymaps()` とかをなんかするっぽい
