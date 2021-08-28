# 加载文件

```python

import os
import yaml


def load_yaml():
    """获取config对象
    为什么加入这个函数呢？主要是因为有些库带有一些自己的数据，此外，可以设置库的默认数据文件，
    这样可以在用户不传数据文件时也能有一个默认的功能
    """
    current_dir = os.path.dirname(__file__)
    config_path = os.path.join(current_dir, 'conf/config.yaml')
    with open(config_path, 'r', encoding='utf-8') as conf:
        default_config = yaml.load(conf, yaml.SafeLoader)
    return default_config
```
