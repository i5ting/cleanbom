# cleanbom


## 编译Java产生 illegal character: \65279 错误的问题

是由于Windows系统开发的编码为UTF-8(BOM)导致，BOM是Byte-Order Mark的意思。一种为了让编辑器自动识别编码。在文件前3个字节加上了EE,BB,BF，但标准的UTF-8（Linux不支持BOM）编码并不会这样做。

## 步骤

1. 遍历当前目录
1. 找找bom文件，如果是，在文件前3个字节移除EE,BB,BF

## todo

- 判断是否是bom文件
- 移除字节
- 写成cli


