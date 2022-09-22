# Oracle JDK 与Open JDK 区别及版本选择

## JDK下载
- [Oracle JDK下载地址](https://www.oracle.com/java/technologies/downloads/archive/)
- [Open JDK下载地址](https://adoptopenjdk.net/)
---

## 收费免费区别
- 协议路径：BCL -> OTN -> NFTC
```
允许商用
BCL： Oracle Binary Code License Agreement for the Java SE Platform Products and JavaFX

不允许商用
OTN： Oracle Technology Network License Agreement for Oracle Java SE

LTS: 长期支持
```

- NFTC 协议内容
1.  JDK17确实可以免费商用，时间截止到2024年9月，共计3年。完整的许可协议在这里（[NFTC](https://www.oracle.com/downloads/licenses/no-fee-license.html)），既在符合美国进出口限制的情况下，开发者既可以在内部使用JDK17，也可以发布给客户使用。需要指出这个许可协议是通用的，并不针对JDK17，只有在JDK17的下载页中给出了说明，内容如下。也就是说JDK17是Oracle Java中的一个特例，之前的版本维持原状。==注意这个免费是没有订阅服务的，Oracle的订阅服务是要收费的.==
2. 此外Oracle启动了LTS长期版本设计，==目前看是3年（以后是2年），在下一个LTS版本出现后，前一个NFTC许可的LTS会至少保持1年。==LTS最少8年（其中3年免费商用，5年收费商用）。在Oracle的FAQ中指出：JDK17之后的版本都遵守NFTC协议（免费），但是有时间期限，免费期之后会收费（OTN）。非NFTC协议的JDK，例如JDK18，6个月内可以免费。


---

## Open Jdk
- 无论是Oracle’s OpenJDK，还是Oracle JDK，还是AdoptOpenJDK，实际上都是对OpenJDK项目的源码进行build之后的产物，即JDK binaries。所以其实你自己也可以对OpenJDK的源码进行build，来生成自己的JDK binaries.
- Oracle提供的付费版本的JDK，和Oracle's OpenJDK几乎没有区别，只是Oracle会对Oracle JDK提供长时间的支持服务、安全更新等，而Oracle’s OpenJDK只提供6个月的安全更新服务。

- 想要免费使用Java，建议使用社区提供的AdoptOpenJDK，而不是Oracle‘s OpenJDK，因为后者只提供六个月的更新服务，而前者会提供几年的服务。

---



参考：
- [Oracle JDK究竟从哪个版本开始收费？](https://www.cnblogs.com/xuruiming/p/12881503.html)
- [Open JDK 的准确由来](https://zhuanlan.zhihu.com/p/114623519)
- [Oracle JDK17及以后的版本真的都免费么?](https://zhuanlan.zhihu.com/p/414822476)