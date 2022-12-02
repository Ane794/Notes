# [ycm-core/YouCompleteMe](https://github.com/ycm-core/YouCompleteMe)

## 安裝

在軟件根目錄下, 執行:

```sh
python -m install
```

### 問題

#### CMake 錯誤 "Unknown compiler - C++17 filesystem library missing"

子模塊 [`ycm-core/ycmd@ece414c`] 需要庫 `filesystem`, 但部分系統沒有;
切換 [`ycm-core/ycmd`] 到更早的分支以解決問題:

```sh
cd third_party/ycmd
git checkout cb1e310
git submodule update --init --recursive
```

[`ycm-core/ycmd@ece414c`]: https://github.com/ycm-core/ycmd/commit/ece414c8c01fe9bf83f3752db00a4a589a3a14cb
[`ycm-core/ycmd`]: https://github.com/ycm-core/ycmd
