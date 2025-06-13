# koishi-plugin-mememaker

[![npm](https://img.shields.io/npm/v/koishi-plugin-mememaker?style=flat-square)](https://www.npmjs.com/package/koishi-plugin-mememaker)

## 如你所见，↓这是预览效果
![img](http://ninjas-get.000.pe/Assets/MMMakerPreview/preview2.png)

## 使用方法
如你所见，你可以通过以下命令使用本插件：
- 使用 自动翻译 来翻译文字：
  ```
  入典 <文字>
  ```
- 使用 \`-n\` 参数指定翻译后的文字：
  ```
  入典 <文字> -n <翻译的文字>
  ```
---

## 究竟是谁在迫害风切（

### 我不是 我没有）

### 普通用户可以不看这里
<details>
<summary>如何将这个方法使用到你自己的插件</summary>
如果你真的足够闲，想把这个辣鸡方法使用到你自己的插件：<br>
作为依赖类使用时，导入RuDian类，创建一个新对象，参数为ctx，<br>
然后使用RDOne方法即可，<br>
传入参数为imageURL，上段文字，下段文字

-
关于为什么是RDOne————因为RDTwo要等我更新（
使用示例：

```
import { RuDian as rd } from 'koishi-plugin-mememaker';
export function apply(ctx: Context, config: Config) {
  ctx.command('test', 'test')
     .action(async ({ session }) => {
        const rd1 = new rd(ctx)
        session.send(await rd1.RDOne('http://example.com','测c试','测j试'))
    })
}
```

调用此方法后，就会返回生成的图片，你可以选择session.send(记得await)或return它。

</details>

## 更新日志

<details>
<summary>点击此处 查看更新日志</summary>

- **1.0.23**    翻译API换了一个。

- **1.0.22**    翻译API换了一个。输入语言不局限于中文，自定义输出翻译为别的语言。

- **1.0.21**    翻译API寄了，换了一个。暂时只支持输入`中文`，输出翻译为别的语言。

- **1.0.19**    优化README与控制台显示效果及说明文字（子规不要使用老版本开发了咪。。。）

- **1.0.17**    适配后端翻译API的返回数据的结构改变

- **1.0.16**    对被提交的尚未完成的功能进行了修复

- **1.0.15**    修复了更新日志

- **1.0.14**    修复并增加了一些小问题

- **1.0.13**    调整了结构，对github文件遗漏的部分进行了同步

- **1.0.12**    优化在`onebot`平台的`回复`时触发`入典 十二进制串行计数器 -n`，误将图片元素作为翻译的情况

- **1.0.11**    优化各种小细节
    -   优化处理触发指令，但是未输入具体内容的情况
    -   优化回复生成时，`onebot`平台回复的图片元素作为输入的意外情况
    -   优化日志输出打印，改用`logger`
    -   优化README与控制台显示效果及说明文字
    -   新增配置项`loggerinfo`，用于调试日志输出
    -   开发者增加~

- **1.0.10**    新增过小图片会自动放大避免字体过糊（感谢子规佬）

- **1.0.9**     增加了插件主页

- **1.0.8**     增加两种新的交互方式

- **1.0.7**     修复错误的版本限制，同时兼容puppeteer和canvas的canvas服务

- **1.0.6**     修复字体过小的问题

- **1.0.5**     更改预览图错误的问题

- **1.0.4**     新增白嫖的翻译API，可以自动翻译文字

- **1.0.3**     导出RuDian类，使插件可以作为依赖被调用

- **1.0.2**     对图片大小做了适配，对迫害风切的部分进行了补偿（

- **1.0.1**     增加依赖项

</details>