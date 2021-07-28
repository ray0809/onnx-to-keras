# onnx2keras

This is a tool for converting onnx models (as exported by for example pytorch) into tensorflow keras 
models. It focuses on inference performance and what we call high-level-compatibility rather than 
completeness. That is, it will not be able to convert every onnx model, but the models it can convert 
it will convert in a nice way. With high-level-compatibility we mean that the converted models produced
are constructed using the high-level keras API and should be similar to how the model would have 
been implemented in keras if it was implemented by hand.

Usage
-----
核心的op转换都在onnx2keras.py文件中，可以详细阅读
```bash
# 转换过程可能出现op不支持，需要边实验边补充
python onnx2keras.py xxx.onnx xxx.h5 
```
