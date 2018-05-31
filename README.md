# FastEC
### Android通用框架设计与完整电商APP

1. latte-annotations：注解model-提供代码生成器所需注解
                      类型为Java Library
2. latte-compiler：代码生成器model-从注解获取信息，通过annotationProcessor或apt生成代码
                   类型为Java Library
3. latte-core：核心model-路由架构、HTTP请求、照相和二维码及图片剪裁、具有共性的通用UI、通用工具、WebView处理
               微信登录和支付封装、支付宝支付封装、诸多重复性的处理
               类型为Android Library
               依赖latte-annotations
4. latte-ec：业务model-相应一类业务的特殊UI、相应一类业务需要的通用逻辑、相应一类业务的特殊处理
             类型为Android Library
             依赖latte-core
5. latte-example：项目model-项目特有的个别功能、只有该项目需要的第三方库、只有该项目会更改的UI及逻辑
                  需要在application model中使用的一些签名和验证
                  类型为Android Application
                  依赖latte-ec
                  依赖latte-compiler
                  
![image](https://github.com/wuchao226/FastEC/blob/master/images/preview.gif)
