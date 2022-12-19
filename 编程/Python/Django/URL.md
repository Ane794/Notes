# Django URL

## 轉發 URL

### 依賴

- django-revproxy

### 代碼

```python
""" urls.py """

from django.urls import re_path
from revproxy.views import ProxyView

urlpatterns = [
    re_path(r'^foo/bar/(?P<path>.*)', ProxyView.as_view(upstream='http://dest.url:port/etc/')),
]
```
