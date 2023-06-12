# project-anti-jeecg
列数 jeecg 各大罪状; 以及我推荐 ruoyi-pro 的理由

+ 项目过于臃肿, 什么功能都有, 什么功能都不好用
+ pom文件依赖复杂, 用来二开极易导致依赖冲突
+ 权限设计非常冗余且耦合, 实现逻辑极其非常超级复杂, 一个简单的RBAC, 使用了各种切面/登录状态/token等等各种实现
+ 只支持 mysql; 对 postgres, oracle 需要自己适配
+ 字典翻译是通过后端切面实现的, 消耗性能, 复杂度高
+ 多租户是通过 mybatisInterceptor 再查询一次租户 id 实现的; 表字段冗余, 且索引困难
+ createTime, updateTime, delFlag 命名极不符合英文习惯
+ 
