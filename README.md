# keras修改后端框架

1. 修改配置文件
指定"backend": "tensorflow",或者 "theano"
```python
{
	"image_dim_ordering": "tf",
	"epsilon": 1e-07,
	"floatx": "float32",
	"backend": "tensorflow"
}
```

2. 每次导入keras前，修改配置
```python
import os
os.environ['KERAS_BACKEND']='tensorflow'
import keras
```

3. 修改环境变量

```python

KERAS_BACKEND=tensorflow python3 -c "from keras import backend"

```
