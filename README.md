jfinal-utils
============

jfinal  utils，查看其他插件-> [Maven](http://search.maven.org/#search%7Cga%7C1%7Ccn.dreampie)

maven 引用  ${jfinal-utils.version}替换为相应的版本如:0.2

```xml
<dependency>
 <groupId>cn.dreampie</groupId>
 <artifactId>jfinal-utils</artifactId>
 <version>${jfinal-utils.version}</version>
</dependency>
```

加密工具类
```java

//md5加密
EncriptionKit.encrypt(string)

//文本hash加密 salt是加密密钥
EncriptionKit.textEncrypt(string，salt)
//文本hash解密
EncriptionKit.textDecrypt(string，salt)

```
url匹配工具，shiro的url过滤使用

```java

AntPathMatcher antPathMatcher = new AntPathMatcher();
//判断url是否匹配
antPathMatcher.match(srcUrl, destUrl)

```

freemarker模板解析工具

```java

FreemarkerLoader  loader= new  FreemarkerLoader("/template",filepath);
loader.setValue(key,value);
loader.getHtml()

```

class文件扫描工具类

```java

ClassSearchKit.of(Model.class).includepaths(includeClassPaths).search();

```

正则验证

```java

//判断空
ValidateKit.isNullOrEmpty(string)

//支持电话，手机，邮件，邮编，中文，字母，数字，正整数等等...请看源码
```
