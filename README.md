# AesEncrypt
用C++开源库cryptopp 封装的Aes对称加密

# 什么是AES？
那么为什么原来的DES会被取代呢，，原因就在于其使用56位密钥，比较容易被破解。而AES可以使用128、192、和256位密钥，并且用128位分组加密和解密数据，相对来说安全很多。完善的加密算法在理论上是无法破解的，除非使用穷尽法。使用穷尽法破解密钥长度在128位以上的加密数据是不现实的，仅存在理论上的可能性。统计显示，即使使用目前世界上运算速度最快的计算机，穷尽128位密钥也要花上几十亿年的时间，更不用说去破解采用256位密钥长度的AES算法了。

# 使用
- 在项目的build.gradle 下面添加仓库地址
```
allprojects {
    repositories {
        google()
        jcenter()
        maven { url "https://github.com/oceanhub168pub/maven_repo/raw/master" }  // 这一句
    }
}
```

- 在项目中引用
> api 'com.hub168.yh:AesEncryop-android:1.0.0@aar'

- 方法

    // 加密
    public static native byte[] nativeEncryptStr(byte[] plainText, byte[] pwdBytes);
    
    
    // 解密
    public static native byte[] nativeDecryptStr(byte[] plainText, byte[] pwdBytes);
