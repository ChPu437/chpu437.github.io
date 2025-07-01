## 添加新闻
在网站首页右侧新闻栏添加新闻条目
### 操作步骤
在data/news.yml文件中复制之前的一条新闻条目代码，粘贴后修改，以下面这个条目的代码为例：
```yml
- date: Apr. 9, 2025
  headline: "2022,2023,2024 's companionship activity:<a href='https://mp.weixin.qq.com/s/84ZTnxK51wXLjL07DgKX1g' target='_blank'>link</a>"

```

## 添加小组活动照片
在Gallery页面添加图片
### 操作步骤
在data/pics.yml文件中 ourgroup 复制之前的一条图片条目代码，粘贴后修改，以下面这个条目的代码为例：
- id：日期+活动名
- image：
  - 命名：日期 + 活动
  - 尺寸：2048 * 1152 像素
  - 图片存放目录：seu-netsi.github.io/images/gallery
- intro：会展示在图片下方的图片介绍
  

```yml
- id: 2022_10_19_09J221_First_Event2
    image: 2212.jpg
    intro: "09J221 first meeting"
    date: "2022-10-19"
```