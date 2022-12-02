# Arch Linux foobar2000 (Wine)

## 問題

### 無法播放聲音

刚安装好的 `foobar2000` 无法找到音频设备, 这是因为 `Wine` 后端调用 `PulseAudio` 模块来提供声音支持,  
而 `foobar2000` 只有 32 位版本.  
默认情况下, 在 `Arch Linux` 中安装 `Wine`, 会顺带装上 32 位的库, 但偏偏没安装 `PulseAudio`. 因此要我们自己来补漏:

```sh
sudo pacman -S lib32-libpulse
```

之后就可以在Foobar2000中选择PulseAudio作为输出了.

参考: [https://bbs.archlinux.org/viewtopic.php?id=227993]

[https://bbs.archlinux.org/viewtopic.php?id=227993]: [https://bbs.archlinux.org/viewtopic.php?id=227993]
