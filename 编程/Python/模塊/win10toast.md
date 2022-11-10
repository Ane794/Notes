# win10toast

显示 Windows 10 消息.

```python
from win10toast import ToastNotifier

ToastNotifier().show_toast(
    'Notification',  # 标题
    'Here coms the message',  # 消息内容
    duration=0,  # 保留通知的时长; 结束前程序不会终止.
)
```
