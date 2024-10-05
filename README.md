# IPTV-ChinaTelecom-Zhejiang-Hangzhou

## 简介

为了实现让更多的设备可以使用浙江电信（杭州）的IPTV播放，并且可以在外网或者其他网路下收看的需求。

尤其是最近电视家之类的直播软件被下架了很多，通过电信的IPTV收看电视信号，稳定很多。

**痛点解决：**

- 父母想看电视节目，但是又不想开通有线电视
- 网上找来的直播源不稳定，用起来很不爽
- 很多直播源缺少很多电视台，太不清晰

**本方案的缺点：**

- 需要个软路由或者小机器一直跑着，譬如OpenWRT，NAS的Docker
- 需要有些动手能力
    - 如果软路由有 > 2的网口，则比较容易
    - 如果软路由只有两个网口
        - 则需要电信光猫的控制台密码
        - 或者可以使用USB的扩展网口



具体实现方式，可以参考：

https://xiking.win/2021/06/20/4-use-iptv-in-multiple-devices/

https://github.com/luckyyyyy/blog/issues/75

我写得估计没人家好 😂

## 本项目提供的内容

假如你根据教程搭建好组播转单播的话，就需要播放的频道的列表了，这就是本项目提供的内容了。

去除了那些重复的频道，并且是低分辨率的。如果FHD的清晰度下没有的，则保留。去除了购物频道，个人厌恶购物频道。

理论上，浙江省电信基本都通用，可以测试一下。

台标 和 电视节目的EPG 都已经配置在了m3u文件里了。导入就能自动配置。

多说一句，如果你使用OpenWRT，推荐msd_lite替代udpxy，问题少一点，性能好一点😜



==**欢迎大家来一起贡献，欢迎提交PR，如果喜欢本项目，请Star**==



## 最近抓取

**时间：**2024-12-04

## 操作步骤

1. 下载china_telecom_iptv.m3u到你本地，或者Fork一下本项目。
2. 注意修改{{}}格式的内容，譬如：
    1. {{路由器地址必须替换}} - 你架设msd_lite或者udpxy的机器的地址
    2. {{端口必须替换}} - 你的msd_lite或者udpxy端口
3. 测试一下是否能够播放（单个地址也行，整个列表也可以）
    1. **Windows**：[PotPlayer](https://potplayer.daum.net/)
    2. **macOS**: [IINA](https://iina.io/)
4. 推荐的播放器
    1. **macOS**: 
        1. APTV ❤️👍🏼：https://apps.apple.com/tw/app/aptv/id1630403500 （很好，我买了高级服务，可以免费用）
        2. zFuse: https://apps.apple.com/tw/app/zfuse-%E5%BD%B1%E7%89%87%E6%92%AD%E6%94%BE%E5%99%A8/id1009747025
    2. **Apple TV:** 
        1. APTV ❤️👍🏼：https://apps.apple.com/tw/app/aptv/id1630403500
    3. Android TV: (两个都只能凑合，不完美)
        1. Tivimate Player ❤️: https://tivimate.com/
        2. 我的电视❤️: https://github.com/lizongying/my-tv
    4. **Windows**：[PotPlayer](https://potplayer.daum.net/)



## 如何获取的？

首先，感谢其他人的贡献，譬如：[c1pher-cn](https://github.com/c1pher-cn) 等等，没有他们分享，我也很难整理的比较全面。

其次，[黑鸟播放器](https://guihet.com/blackbird-player.html)用来扫描源地址非常好用。

## 鸣谢

[c1pher-cn](https://github.com/c1pher-cn) - 提供的杭州电信的播放列表的参考

[William Chan/luckyyyyy](https://github.com/luckyyyyy) - 教会我如何实现电信IPTV的组播转单播，VLAN的操作等等

[Pixman](https://pixman.io/) - 提供了相当一大部分的台标和EPG

[肥羊直播](https://tools.v1.mk/) - 提供了其他很难找到的台标和格式转换器

[黑鸟播放器](https://guihet.com/blackbird-player.html) - 相当方便的扫描源地址工具

[浙江电信](https://www.189.cn/) - 提供的IPTV服务和很多不错的频道

## 其他推荐

[Pixman](https://pixman.io/) - coding做的非常好的IPTV内容提供

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=yangwudong/IPTV-ChinaTelecom-Zhejiang-Hangzhou&type=Date)](https://star-history.com/#yangwudong/IPTV-ChinaTelecom-Zhejiang-Hangzhou&Date)