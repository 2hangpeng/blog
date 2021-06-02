# SiriKit 人机界面指南

**本文为译文，原文连接：**[**Human Interface Guidelines-Siri**](https://developer.apple.com/design/human-interface-guidelines/ios/system-capabilities/siri/)

你的应用可以通过集成Siri，以响应用户的语音命令和问题，完成某些任务。Siri对语言进行处理并进行语义分析，将这些语音指令转换成应用程序可以处理的指令。应用程序定义它支持的任务，验证收到的信息，提供Siri提供信息，执行操作。应用程序的响应由 `Siri` 反馈，并且呈现在 `Siri` 界面中。如果可以的话，你的应用程序可以为Siri提供一个定制的用户界面来展示。例如，健身应用可能会提供定制的健身信息。

**争取一种不需要触摸或是查看屏幕的语音操作体验。** 人们可以通过耳机，汽车或是在房间的另一头与Siri互动。尽可能地让用户在不解锁手机的情况下完成任务。

**不要试图模仿或操纵Siri。** 你的应用程序永远不应该模仿Siri，试图复制Siri提供的功能，或者提供看上去来自苹果的响应。

**适当的内容。** 绝不要包含可能冒犯或侮辱的内容。

**不做广告。** 你的应用程序的Siri体验不应该包括广告、营销或应用内购买销售推销。

## 支持的交互

提供以下服务的iOS应用程序可以与Siri集成。

| 服务 | 支持的交互 |
| :--- | :--- |
| 音视频通话 | 拨打电话 搜索通话记录 |
| CarPlay集成 | 激活并保存司机的设置。 切换汽车的音乐。 改变汽车的空调设置。 改变汽车的除霜设置。 改变汽车的座位设置。 切换汽车的收音机频道。 |
| 健身活动 | 开始、暂停、恢复、结束、取消训练。 |
| 待办的事和笔记 | 创建待办事项列表和项目。 搜索待办事项列表和项目。 将待办事项列表项标记为完成。 根据日期、时间和/或位置创建提醒。 创建笔记。 搜索笔记。 修改笔记。 |
| 信息 | 发送消息。 读取接收到的消息。 搜索信息。 |
| 支付 | 发起付款。 请求支付。 支付账单。 寻找账单。 搜索并查看账户信息，包括余额、点数和英里数。 账户之间的转账。 |
| 相片管理 | 搜索照片并在应用中显示。 |
| 出行预定 | 出行预定。 出行信息查询。 |
| 汽车集成 | 启动危险信号灯或按喇叭。 打开关闭车门。 检查当前的燃料或功率。 |
| 显示条码 | 显示一个条码，比如二维码或条形码。 |

## 给使用者的反馈

**快速响应，减少交互。** 人们使用Siri是为了方便，并希望得到快速响应。提出有效的、有重点的选择，减少额外提示的可能性。

**让人们直接了解内容。** 从Siri到应用程序的转换应该直接完成预期的目的。不要显示中间的屏幕或信息来降低体验。

**相关的和准确的。** 使你的应用程序的响应与用户当前的请求和期望相关。例如，如果用户要求Siri用你的应用发送一条消息，发送一条消息。不要做不同的动作。

**当请求与财务相关时，默认使用最安全、花费最少的的选项。** 绝不要欺骗用户或歪曲信息。当购物时有多个价格时，不要默认为最昂贵的。当用户正在付款时，不要在没有通知他们的情况下收取额外费用。

## 设计一个自定义界面

**确保你的界面与Siri很好地融合在一起。** 使用你的应用程序的颜色、图像和其他设计元素来传达你的品牌是很好的，但任何界面元素都应该让人感觉它们属于Siri。除非你的应用需要一个完全定制的界面，否则请将你的内容集成到Siri提供的默认界面中。

**提供足够的间距和边距。** 避免将内容扩展到界面的边缘，除非它的内容看起来像地图一样自然地流出屏幕。通常，在界面的每条边和内容之间提供至少几个像素的空白。使用界面顶部的app图标进行对齐指导。当与此图标的中心对齐时，内容往往会显示得很好。

**最小化界面的高度。** 理想情况下，您的界面不应该高于屏幕的高度，这样用户就可以在不滚动的情况下看到所有内容。

**不要创建一个具有交互性的界面。** 你的界面不能对手势做出反应——除了会打开你的应用程序的点击——或者在Siri中显示其他事件，所以要避免显示互动的图像或形状。

**不要在你的界面中包含你的应用程序名称或图标。** 系统自动显示这些信息。

## 提高准确性

**如果可以的话，定义自定义词汇表。** 通过定义人们可能在请求中实际使用的特定术语，如账户名、联系人姓名、照片标签、相册名称、乘车选项和健身名称，帮助Siri了解你的应用程序执行的更多操作。这些术语应该是非通用的，并且是你的应用程序独有的。不要包括其他应用程序名称、明显与其他应用程序相关的术语、不恰当的语言或保留的短语，比如“嘿，Siri”。请注意，你定义的任何术语都是Siri用来帮助解决请求的，但不能保证被识别。

**考虑定义备用的应用程序名称。** 如果人们对你的应用程序名字的发音有所不同，你可以提供一个可供选择的名字列表，以增加你用Siri定位应用程序时的灵活性。例如，一个UnicornChat应用程序可能会将术语Unicorn定义为另一个应用程序名称。不要将其他应用程序名称作为你应用程序的替代名称。

**提供请求示例。** 提供一些用于展示在 Siri 帮助界面中的事例短语。用这些短语来教人们用你的应用程序使用Siri的最简单、最有效的方法。

## 附

1. [SiriKit](https://developer.apple.com/documentation/sirikit?language=objc)
2. [Human Interface Guidelines-Siri](https://developer.apple.com/design/human-interface-guidelines/ios/system-capabilities/siri/)

> Title: SiriKit 人机界面指南
>
> Date: 2018.07.03
>
> Author: zhangpeng
>
> Github: [https://github.com/gh-zhangpeng](https://github.com/gh-zhangpeng)
