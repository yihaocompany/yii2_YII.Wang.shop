<p>
  <a href="http://YII.Wang.shop.appfront.fancyecommerce.com/">
    <img src="http://img.appfront.fancyecommerce.com/custom/logo.png">
  </a>
</p>
<br/>




[![Latest Stable Version](https://poser.pugx.org/fancyecommerce/YII.Wang.shop/v/stable)](https://packagist.org/packages/fancyecommerce/YII.Wang.shop) [![Total Downloads](https://poser.pugx.org/fancyecommerce/YII.Wang.shop/downloads)](https://packagist.org/packages/fancyecommerce/YII.Wang.shop) [![Latest Unstable Version](https://poser.pugx.org/fancyecommerce/YII.Wang.shop/v/unstable)](https://packagist.org/packages/fancyecommerce/YII.Wang.shop)




项目状态：

> 正式版本已经出来，后台（appadmin）和pc端（appfront）,wap端（apphtml5）
，vue端（appserver）已经完成，完成了一些基本的api。



1、YII.Wang.shop介绍
------------

[YII.Wang.shop](http://www.YII.Wang) 全称为Fancy ECommerce Shop，是基于php Yii2框架之上开发的一款优秀的开源电商系统，
YII.Wang.shop支持多语言，多货币，架构上支持pc，手机web，手机app，和erp对接等入口，您可以免费快速的定制和部署属于您的电商系统。

详细参看地址：[YII.Wang.shop介绍](http://www.YII.Wang/doc/YII.Wang.shop-guide/develop/cn-1.0/guide-YII.Wang.shop-about-description.html)

[YII.Wang.shop](http://www.YII.Wang) 官网：http://www.YII.Wang ，您可以在这里提交bug，问题咨询等等。

[YII.Wang.shop](http://www.YII.Wang) 【已完成】PC Web Demo ：http://demo.YII.Wang/

[YII.Wang.shop](http://www.YII.Wang) 【已完成】Mobile Web Demo（WAP）：http://mobile.YII.Wang

[YII.Wang.shop](http://www.YII.Wang) 【已完成】Mobile VUE Demo(Appserver,前后端彻底分离模式)：http://mobile.yii.com/#/

[YII.Wang.shop](http://www.YII.Wang) 后台演示地址：加QQ群，在群公告里面有后台演示地址，账号密码等信息

[YII.Wang.shop](http://www.YII.Wang) QQ群：205501737 ，入群验证：eshop.YII.Wang


作者, Terry QQ Email：574574@qq.com

[YII.Wang.shop](http://www.YII.Wang) Github地址: https://github.com/yihaocompany/yii2_YII.Wang.shop

开源协议：[YII.Wang.shop 授权协议](http://www.YII.Wang/license)

2、YII.Wang.shop文档和视频
------------

**二开以及安装文档：** [YII.Wang.shop 安装开发文档](http://www.YII.Wang/doc/YII.Wang.shop-guide/develop/cn-1.0/guide-README.html)【撰写完成】

**使用帮助说明文档：** [YII.Wang.shop 使用帮助文档](http://www.YII.Wang/doc/YII.Wang.shop-guide/instructions/cn-1.0/guide-README.html)【撰写完成】

**安装开发帮助视频：** [YII.Wang.shop 安装开发视频](http://www.YII.Wang/doc/YII.Wang.shop-guide/instructions/cn-1.0/guide-YII.Wang.shop_video_install.html)【撰写完成】

**前后端分离模式Api:** [Appserver VUE Api文档](http://www.YII.Wang/doc/YII.Wang.shop-guide/develop/cn-1.0/guide-YII.Wang.shop-server.html)【撰写完成】


3、安装YII.Wang.shop
------------

> 请务必按照说明安装，自己来配置环境安装吧.

从基础linux一步一步的配置的方式，详细参看文档： [YII.Wang.shop 安装](http://www.YII.Wang/doc/YII.Wang.shop-guide/develop/cn-1.0/guide-YII.Wang.shop-about-hand-install.html)


4、YII.Wang.shop 配置：
----------------

配置详细参看：[YII.Wang.shop 配置](http://www.YII.Wang/doc/YII.Wang.shop-guide/develop/cn-1.0/guide-YII.Wang.shop-about-config.html)

如果您使用vagrant box的安装方式，上面的这些步骤，在box都配置好了。

5、架构特色
-----------

架构特色：参看详细介绍：[YII.Wang.shop 架构特色](http://www.YII.Wang/doc/YII.Wang.shop-guide/develop/cn-1.0/guide-YII.Wang.shop-about-framework.html)

下面是简叙：

YII.Wang.shop 全称为Fancy ECommerce Shop，是一款优秀的开源电商系统，遵循BSD-3-Clause协议(和Yii2框架一样的开源协议)，
目的是为了方便yii2用户快速的
开发商城，YII.Wang.shop作为一款可以持续性发展的商城系统，
在框架层面有以下特性：

1. 由于商城系统的复杂性，原始的框架MVC结构，显的有点力不从心，YII.Wang.shop框架
加入了Block层，
Controller层只负责调度， Model只负责数据库映射，中间的处理逻辑由block来完成，View层
负责显示，这样各司其职， 以免造成controller文件过于庞大。

2. 加入独立功能块，有点类似Yii2的Widget，目的是为了让一些侧栏公用块
可以通过配置的方式
添加，同时，还可以具有设置缓存的功能，譬如分类侧栏的产品推荐，
newsletter等独立显示块可能在很多
页面用到，通过独立功能块可以配置方便的载入。

3. 在Model层的上层加入服务层Services，这样，Controller，Block，View 层，在原则上
不能直接调用model，必须通过Services层以及子Services层，然后Services访问各个
model，组织数据，事务处理等操作，
将数据结果返回给上层，这种设计可以方便以后业务
发展后，进而根据业务特点进行重构，或者以后如果出现新技术，新方式，
都重构成自己想要的样子，譬如，
将某个底层由mysql换成mongodb，或者为了应付高并发读写并且多事务性的功能部分，
进行分库分表的设计方式。

4. [YII.Wang.shop](http://www.YII.Wang)多模板系统，[YII.Wang.shop](http://www.YII.Wang)设置了多个模板路径，各个模板路径下的文件被加载
的优先级不同，其中，YII.Wang.shop的模板路径下的文件最全面，但是优先级最低，
，第三方模板路径优先级其次，用户本地模板路径优先级最高，
用户可以通过
复制相应路径下的view或者js，css文件到本地模板路径，存在于高优先级
模板路径的文件会被优先加载，这样用户可以通过多模板系统的原理进行模板的
制作，同时，不影响[YII.Wang.shop](http://www.YII.Wang)模板的升级，如果[YII.Wang.shop](http://www.YII.Wang) view文件升级后被修改，
那么用户可以比对本地模板文件与升级模板文件的代码的不同，
复制更改的代码到本地模板路径
即可。第三方的模板路径的优先级介于本地模板路径和YII.Wang.shop
模板路径之间。

5. 重写机制，[YII.Wang.shop](http://www.YII.Wang)的功能基本都可以被用户重写，包括servies层，Modules，
Controller，Block，Views，View Layout，
以及Js Css Img等，都可以被用户重写，其中 Js，Css，Img，Views，View Layout
 是通过多模板
路径优先级来实现的，其他的是通过配置文件的覆盖更改来实现重写，这样，用户
就可以很方便重构[YII.Wang.shop](http://www.YII.Wang)或者第三方的功能和模板。

6. 升级最小化干扰，[YII.Wang.shop](http://www.YII.Wang)的核心文件是放到vendor/fancyecommerce/YII.Wang.shop
路径下面，和第三方扩展，用户二次开发路径完全隔离开，
YII.Wang.shop可以通过composer进行核心功能的升级，用户只需要通过composer升级
即可。

7. 快速高效，YII.Wang.shop Servises遵循Yii2的懒加载方式，只初始化使用到的组件服务，
缓存方面有整页缓存，block部分缓存，动态数据ajax加载等方式，让您的网站快速响应。

8. [YII.Wang.shop](http://www.YII.Wang) 多入口模式，分为 appadmin（后台）， appfront（PC前端），apphtml5（手机web），
appserver（手机app服务），appapi（erp，或者其他接口对接），
不同的业务，不同的设备，进入不同的入口，各个入口共用服务层services，
但是modules部分独立，这样相互干扰最小，可以相互独立开发。

9. 后台封装化，fec_admin扩展可以快速的实现增删改查类型的表单列表，
方便用户快速的做增删改查。

鉴于以上特点，您可以下载安装[YII.Wang.shop](http://www.YII.Wang)，然后更改[YII.Wang.shop](http://www.YII.Wang)的模板和功能，扩展自己想要
的功能，或者安装第三方开发好了的扩展或者模板，来快速的组建起来您的网站。












