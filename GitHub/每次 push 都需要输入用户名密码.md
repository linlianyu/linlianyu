# 每次 push 都需要输入用户名密码

---

## 前记

&#8195;&#8195;本文借鉴自[《方法1》](https://blog.csdn.net/weixin_41728561/article/details/81478414)

---

- 在命令行执行下面代码，之后再次执行git push 和 git pull 时还需要输入用户名和密码，但是下一次就不需要了

```
git config --global credential.helper store
```
