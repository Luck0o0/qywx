# qywx-spring-boot-starter
企业微信API封装
``` 
<dependency>
  <groupId>com.github.shuaidd</groupId>
  <artifactId>qywx-spring-boot-starter</artifactId>
  <version>2.1.0</version>
</dependency>

```

使用示例
``` 
配置application.yml

qywx:
  corp-id: xxxx（企业号）
  application-list:
  - secret: Kx4sovYN5C0_MEzPY0cOymwbMhGmqdA9VjMFHrAKjdE
    agentId: 1000003
    application-name: little-helper
  - secret: DXB-FXVZNkLGUlLaIJy6CK67WD-dpN1HnPLIzNPo0N4
    agentId: 1000004
    application-name: reporter
  - secret: AfjvAed_ulqhK0OqTprDQ6xOSnqaT34ll2LsRe0D2NA
    application-name: address-book
  url: https://qyapi.weixin.qq.com
  public-path: cgi-bin

```
``` 
public class WeChatTest extends BaseTest {

    /**
    * 查询用户信息
    */
    @Test
    public void getUser(){
        weChatManager.addressBookService().getUser("13259220281", "address-book");
    }
}

实例 可以查看 qywx-spring-boot-example 模块
```
