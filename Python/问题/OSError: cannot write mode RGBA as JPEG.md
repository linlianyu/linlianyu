# OSError: cannot write mode RGBA as JPEG

---

## 前记

&#8195;&#8195;本文借鉴自[OSError: cannot write mode RGBA as JPEG](https://blog.csdn.net/weixin_39777626/article/details/82774270)

---

## 代码

```
image1 = Image.new('RGBA', (20, 20), 'red')
image1.save('REDImage.jpg')
image2 = Image.new('RGBA', (200, 20))
image2.save('TransparentImage.jpg')
```

## 错误信息

```
OSError: cannot write mode RGBA as JPEG
```

## 原因

- RGBA意思是红色，绿色，蓝色，Alpha的色彩空间，Alpha指透明度。而JPG不支持透明度，所以要么丢弃Alpha,要么保存为.png文件

## 解决方法1

```
image1 = Image.new('RGB', (20, 20), 'red')
image1.save('REDImage.jpg')
```

## 解决方法2

```
image2 = Image.new('RGBA', (200, 20))
image2.save('TransparentImage.png')
```
