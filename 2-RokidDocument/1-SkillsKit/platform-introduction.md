## 技能分类

### 什么是技能

Rokid技能开发工具为用户提供的**各种不同场景下的服务**，我们将他们称之为：**`技能（Skill）`**。比如音乐、百科、天气、新闻等。

通过创建各种各样的Rokid技能，以此触达所有搭载Rokid语音方案设备背后的终端用户，向他们提供各种有趣的服务，比如：

- 问一些具体的问题（“若琪，明天杭州会不会下雨？”）
- 玩语音小游戏（“若琪，我要玩文字猜谜。”）
- 控制智能家居设备（“若琪，把卧室的灯打开。”）
- 播放新闻摘要（“若琪，播放最新的新闻。”）

Rokid技能开发工具包含开发工具、文档、以及丰富的示例代码，能够帮助开发者以最快的速度完成技能的开发。在Rokid沉淀的经验之上，专注于更富有创造性的工作。

### 当前支持的技能种类

不同种类的技能可以用来面对不同的业务场景，这是您在开始创建技能时就需要思考的问题。Rokid技能开发工具提供2个维度的4种技能，根据**开放性**可以将技能分为**`公开技能`**和**`私有技能`**；根据**自定义技能的创建方式**，可将自定义技能分为**`自定义语音交互`**和**`预定义语音交互`**。

<table>
    <tr>
        <th>分类维度</th>
        <th>技能划分</th>
    </tr>
    <tr>
        <td rowspan="2" align="center">开放性</td>
        <td align="center">公开技能</td>
    </tr>
    <tr>
        <td align="center">私有技能</td>
    </tr>
    <tr>
        <td rowspan="2" align="center">自定义技能创建方式</td>
        <td align="center">自定义语音交互</td>
    </tr>
    <tr>
        <td align="center">预定义语音交互</td>
    </tr>
    <tr>
</table>
       

#### 不同开放性的技能

首先，需要决定是将技能开放给所有搭载Rokid方案的设备，还是仅授权自有产品或其他指定产品使用。

##### 公开技能
公开属性的技能将会对所有搭载Rokid语音解决方案的设备开放，终端用户可以通过技能商店轻松开启公开技能。

##### 私有技能
私有属性的技能无法向所有用户开放，仅针对经过授权的企业或个人的特定类型的设备开放。用户需要在被授权的设备上才能够使用私有技能。

<table style="word-break:break-all; word-wrap:break-all;">
    <tr>
        <th></th>
        <th width="48%">公开技能</th>
        <th>私有技能</th>
    </tr>
    <tr>
        <td align="center">定位</td>
        <td align="left"><strong>面向终端用户</strong><br>
对所有搭载Rokid语音解决方案的设备开放，终端用户可以通过在app中轻松开启/关闭公有技能。</td>
        <td align="left"><strong>面向开发者</strong><br>
不面向终端用户开放，仅授权自有产品或其他指定产品使用。终端用户需要在被授权的设备上才能够使用私有技能。</td>
    </tr>
    <tr>
        <td align="center">技能商店展示</td>
        <td align="center">审核通过后展示</td>
        <td align="center">不展示</td>
    </tr>
    <tr>
        <td align="center">平台展示</td>
        <td align="left">默认展示到技能商店供终端用户使用，同时默认展示在【产品管理>技能配置】 中供开发者配置。</td>
        <td align="left">技能拥有者自己确定是否展示：（1）不展示，则仅技能拥有者自己可见；（2）展示，则展示在【产品管理>技能配置】中供开发者配置。</td>
    </tr>
    <tr>
        <td align="center">审核</td>
        <td align="center">需审核</td>
        <td align="center">如果展示，需审核</td>
    </tr>
    <tr>
        <td align="center">第三方开发者申请使用</td>
        <td align="left">第三方开发者可以直接在直接【产品管理>技能配置】中页面直接添加，即可使用到他们的产品中（配置到产品中的公有技能，终端用户无法关闭）。</td>
        <td align="left">第三方开发者在【产品管理>技能配置】中向技能拥有者申请授权或申请购买，经过技能拥有者同意后方可使用到产品中。</td>
    </tr>
    <tr>
        <td align="center">付费</td>
        <td align="center">技能免费使用(技能在使用中部分存在收费项目)</td>
        <td align="center">技能拥有者自己确定技能是否收费</td>
    </tr>
    <tr>
        <td align="center">本地技能</td>
        <td align="center">不支持</td>
        <td align="center">支持</td>
    </tr>
    <tr>
        <td align="center">备注</td>
        <td colspan="2" align="left">在创建<strong><code>私有技能</code></strong>时还需选择是创建<strong><code>本地私有技能</code></strong>还是<strong><code>云端私有技能</code></strong>。<br>创建<strong><code>本地私有技能</code></strong>需要写一个apk推送到设备上（具体参照：<a href="https://github.com/Rokid/NewsDemo">Rokid NativeApp开发示例</a>）；创建<strong><code>云端私有技能</code></strong>，则后台配置服务不在设备上而是在另外搭建的服务端上。<br>不管本地还是云端，都需要遵守我们的<a href="./important-concept/cloud-app-development-protocol_cn.md">协议格式</a>进行通信。（具体参照【技能创建与发布】的第五步-后端服务配置：<a href="./getting-started/create-and-pulibsh.md">技能创建与发布</a>)</td>
    </tr>
</table>

#### 不同创建方式的技能
Rokid技能开发工具，支持自定义技能，开发者根据自己的个性化或业务需求，创建自定义技能。基于创建方式的不同，可以将自定义技能分为自定义语音交互和预定义语音交互。

##### 自定义语音交互
该类型的技能，用户可以对**`语音交互`**进行自定义。具体来说，需要定义：[意图](./important-concept/intend.md)、[用户语句](./important-concept/usersays.md)、[词表](./important-concept/word-list.md)、入口词。

###### 入口词

此外，Rokid还需要通过**`入口词`**来分辨用户是在和技能进行语音交互。用户需要使用含有入口词的语句来唤起技能。比如，为名称为“放个屁”的技能设定入口词为“放个屁”，终端用户就可以用如下语句与技能进行交互了：
>用户：“若琪，打开放个屁”

Rokid将会理解用户的请求，准确进入到“放个屁”的技能中，开始语音交互。

只要在**`语音交互`**中预置了充分的**`用户语句`**、**`词表`**和**`意图`**，并且通过代码在后端服务实现这些意图，自定义技能就能够最大限度地满足预期的用户需求。这种技能最灵活，但也因为需要配置语音交互，而较为复杂。

##### 预定义语音交互
预定义语音交互技能，可以直接引用Rokid已定义好的技能（rokid会不断更新），开发者仅需要在后端服务中直接实现对应的**`意图`**即可。

如果想创建一个听音乐这样的内容类技能，或是能够开关灯、调节空调温度这样用于智能家居设备的技能，可以考虑使用**`预定义语音交互`**。预定义语音交互的技能不完全依赖入口词唤起，因此对用户会更加友好。

> 比如用户可以直接说：“若琪，把房间的灯打开。”来使用智能家居技能。

用户可以在创建技能的第二步【语音交互】环节选择预定义语音交互。（详见[技能创建与发布](./getting-started/create-and-pulibsh.md)）