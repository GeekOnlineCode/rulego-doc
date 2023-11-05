---
home: true
heroImage: /img/logo.png
heroText: RuleGo
tagline: 🚀基于Go语言的轻量级、高性能、嵌入式、可编排组件式的规则引擎
actionText: 快速开始 →
actionLink: /pages/0f6af2/
bannerBg: none

features: # 可选的
- title: 🧩组件化
  details: 一切皆为组件。内置大量组件，你可以灵活配置和重用它们。
- title: ☘️热刷新
  details: 不重启应用情况下，替换或者新增业务逻辑。
- title: ✨轻量化
  details: 资源占用极低。为物联网而生，但远不至于物联网。
- title: 🎯嵌入式
  details: 自研架构，扩展性强。可以无缝集成到项目中。没有依赖任何第三方组件，部署简单。
- title: 📑配置式
  details: 通过配置规则链，搭积木方式实现你高度变化的业务需求。
- title: 🔥应用集成
  details: 可以把RuleGo当做胶水连接各种系统或者协议。


postList: none
hideRightBar: true
---

### 🏆特别用户

::: cardList
```yaml
- name: Sagoo IOT
  desc: 基于Golang开发的企业级开源物联网系统
  avatar: img/sponsors/shaguo.png
  link: https://iotdoc.sagoo.cn/
  bgColor: '#f8c567' # 可选，默认var(--bodyBg)。颜色值有#号时请添加单引号
  textColor: '#1f2328' # 可选，默认var(--textColor)
  expired: '2024-10-07'
```  
:::

<p align="center">
  <a class="become-sponsor iconfont " href="/pages/ccf224">支持这个项目</a>
  <a class="become-sponsor iconfont icon-github " href="https://github.com/rulego/rulego" target="_blank">为RuleGo点星</a>
  <a class="become-sponsor iconfont icon-gitee" href="https://gitee.com/rulego/rulego" target="_blank">为RuleGo点星</a>
</p>

<style>
  .become-sponsor{
    padding: 8px 20px;
    display: inline-block;
    color: #11a8cd;
    border-radius: 30px;
    box-sizing: border-box;
    border: 1px solid #11a8cd;
  }
 .become-sponsor:hover{
    border: 1px solid #13bee8;
    color: #13bee8;
  }
</style>

<br/>


### 🚀特性

* **轻量级：** 无外部中间件依赖，既可以下沉到边缘服务器，实现物联网边缘计算解决方案，也可以部署在云端，作为规则引擎服务。
* **高性能：** 得益于`Go`的高性能特性，另外采用协程池和对象池等技术。对10W条数据进行 **JS脚本过滤->JS脚本数据转换->HTTP推送** 处理,平均用时9秒。
* **嵌入式：** 支持把`RuleGo`嵌入到现有项目，非入侵式利用其特性。
* **组件化：** 所有业务逻辑都是组件，并能灵活配置和重用它们。你也可以把业务地封装成`RuleGo`组件，然后通过搭积木方式实现你高度变化的业务需求。
* **规则链：** 可以灵活地组合和重用不同的组件，实现高度定制化和可扩展性的业务流程。
* **流程编排：** 支持对规则链组件进行动态编排，不重启应用情况下，替换或者新增业务逻辑。
* **扩展简单：** 提供丰富灵活的扩展接口和钩子，如：自定义组件、组件注册管理、规则链解析器、协程池、规则节点执行回调、规则链处理结束回调。
* **动态加载：** 支持通过`Go plugin` 动态加载组件和扩展组件。
* **规则链嵌套：** 支持子规则链嵌套，实现流程复用。
* **内置大量组件：** `消息类型路由`，`脚本路由`，`脚本过滤器`，`脚本转换器`，`HTTP推送`，`MQTT推送`，`发送邮件`，`日志记录`，`数据库操作`
  等组件。可以自行扩展自定义组件。
* **上下文隔离机制：** 可靠的上下文隔离机制，无需担心高并发情况下的数据串流。

### 🎯典型使用场景

* **边缘计算：** 可以在边缘服务器部署`RuleGo`，对数据进行预处理，筛选、聚合或者计算后再上报到云端。数据的处理规则和分发规则可以通过规则链动态配置和修改，而不需要重启系统。
* **物联网：** 收集设备数据上报，经过规则链的规则判断，触发一个或者多个动作，例如：发邮件、发告警、和其他设备或者系统联动。
* **数据分发：** 可以根据不同的消息类型，调用HTTP、MQTT或者gRPC把数据分发到不同系统。
* **应用集成：** 把`RuleGo`当做胶水连接各种系统或者协议，例如：kafka、消息队列、数据库、chatGPT、第三方应用系统。
* **异构系统数据集中处理：** 从不同的数据源（如 MQTT、HTTP 等）接收数据，然后对数据进行过滤、格式转换、然后分发到数据库、业务系统或者仪表板。
* **高度定制化业务：** 把高度定制化或者经常变化的业务解耦出来，交给`RuleGo`规则链进行管理。业务需求变化而不需要重启主程序。
* **复杂业务编排：** 把业务封装成自定义组件，通过`RuleGo`编排和驱动这些自定义的组件，业务逻辑并支持动态调整和替换。
* **微服务编排：** 通过`RuleGo`编排和驱动微服务，或者动态调用第三方服务处理业务，并返回结果。
* **业务代码和业务逻辑解耦：** 例如：用户积分计算系统、风控系统。
* **自动化：** 例如：流程自动化系统、营销自动化系统、对接`大模型`提取用户意图，然后触发规则链与其他系统进行联动或者进行业务处理。
* **灵活配置和高度定制化的事件处理框架：** 对不同的消息类型，进行异步或者同步的处理。

### 🎈代码托管

> **[Gitee](https://gitee.com/rulego/rulego)** | **[Github](https://github.com/rulego/rulego)**

### 🧸参与贡献

欢迎各路好汉一起来参与完善 RuleGo，我们期待你的 PR！

- 贡献代码：代码地址 [RuleGo](https://github.com/rulego/rulego) ，欢迎提交 Issue 或者 Pull Requests
- 维护文档：文档地址 [RuleGo-Doc](https://github.com/rulego/rulego-doc) ，欢迎参与翻译和修订

### 🧲 友情链接
<div class="row">
    <span class="link">
        <a href="https://baomidou.com" target="_blank" title="MybatisPlus">
            <img :src="$withBase('/img/links/mybatis-plus-logo.png')" class="no-zoom">
        </a>
    </span>
    
</div>

<style>
  .link {
    width: 10em;
    text-align: left;
  }
  .link img {
    height:1.8em;
    max-width:180px;
    margin: 14px;
  }
  .row {
    display: flex;
    flex-direction: row;
  }
</style>