# zeal-on-mac
A solution to build Zeal on Apple-Silicon Mac machines

#### The original post is [here](https://github.com/zealdocs/zeal/issues/1372#issuecomment-1063588413) by [@shabbyrobe](https://github.com/shabbyrobe).

Use shabbyrobe's folk instead of the official one since the WebEngine of Qt5 is not compatible with arm64. To solve this issue by using Qt6, modifications are done in repo https://github.com/shabbyrobe/zeal.


### build instructions
```bash
brew install qt@6
brew install libarchive
export CMAKE_PREFIX_PATH="$(brew --prefix qt@6):$(brew --prefix libarchive)"
git clone https://github.com/shabbyrobe/zeal.git
cd zeal
mkdir build
cd build
cmake ..
make -j 8

```

My MacBook Pro 14-inch with m1pro macOS 13.1 works well with these instructions on 30 Dec, 2022.
