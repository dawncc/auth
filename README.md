# Auth

原本为KISSY-Form中的校验组件，gallery拆分之后分离出来作为独立组件置于顶层，从1.4版本开始，其实和1.3代码一样。

v1.5 测试中，请勿使用

## changelog

### V1.5 by 明河

    [!] 重构消息类
    [!] 改用get和set来获取/设置属性
    [!] tag config方式更改
    [!] [Auth] 优先获取name，而不是id
    [!] [Field] el配置改成target
    [!] [Field] 修改event配置
    [!] [Field] validate()方法去掉cfg参数，多个规则逗号隔开
    [!] [Field] 遍历时排除button元素
    [!] [Rule] 重构
    [!] [ruleFactory] 颠倒规则函数的value和pv
    [!] [ruleFactory] 不再区分html规则和自定义规则
    [!] [ruleFactory] 默认规则提取成default.js
    [!] [Msg] 重构
    [!] [Msg] msg传递方式优化
    [!] 去掉多余无用的样式，使用stylus改写
    [!] [Field]修正不存在验证规则时报错的bug

    [+] 新增render()，不再new时马上初始化逻辑
    [+] 增加validate的同名方法test
    [+] 继承promise
    [+] 异步校验支持
    [+] 增加对uploader的支持

    [+] [auth]增加rules属性，用于获取所有的验证规则
    [+] [auth]增加useId属性，可以强制使用id作为字段标识
    [+] [auth]增加submitTest配置，用于拦截表单提交，先触发验证
    [+] [auth]增加fields属性，所有的字段
    [+] [auth]验证前过滤掉不需要验证的字段
    [+] [auth]test()支持指定需要验证的字段，比如test("user,email")
    [+] [auth]增加fieldTarget方法
    [+] [auth]增加field方法

    [+] [Field]增加success、error、beforeTest事件
    [+] [Filed]新增rules属性，用于获取所有的规则
    [+] [Filed]新增exclude配置，用于排除指定规则验证
    [+] [Filed]新增host属性
    [+] [Filed]将Field实例缓存到元素的data-field
    [+] [Filed]增加name属性

    [+] [ruleFactory] 支持批量添加验证规则
    [+] [Rule]规则可以设置默认消息
    [+] [Rule]required组的处理
    [+] [Rule]required清理掉空格
    [+] [Rule]max和min可以处理checkbox的情况
    [+] [Rule]增加mobile、email、date、number支持

    [+] [Msg]兼容服务器返回的错误信息
    [+] [Msg]可以传自定义消息类进去
    [+] [Msg]可以自动生成消息层
    [+] [Msg]默认规则增加msg

    [-] 删除rule/base
    [-] 删除propertyRule
    [-] 删除lib/base

### V1.4

    [!] 从butterfly中迁移到新的gallery