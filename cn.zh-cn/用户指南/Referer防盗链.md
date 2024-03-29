# Referer防盗链<a name="vod010013"></a>

Referer防盗链是基于HTTP协议支持的Referer机制实现的，通过播放请求中携带的Referer字段识别请求来源。配置黑名单或白名单，CDN将根据名单对请求来源进行过滤，从而达到访问控制的目的。您可以参考如下步骤配置Referer防盗链，也可以通过[视频指导](https://bbs.huaweicloud.com/videos/cf87fe1e4eb04c79a56fe71e374441ec)来操作。

## 注意事项<a name="section9354115514113"></a>

-   该功能为可选项，默认不启用。
-   Referer黑名单与Referer白名单互斥，不支持同时设置。
-   黑名单或白名单中的域名最多支持4级域名，且最多支持配置100条。
-   黑名单或白名单中配置的域名前不能带协议名，域名为前缀匹配。如填写“example.example01.com“，则“example.example01.com/123“和“example.example01.com.cn“也会匹配成功。

## 配置步骤<a name="zh-cn_topic_0111450891_section6349446803"></a>

1.  登录[视频点播控制台](https://console.huaweicloud.com/vod)。
2.  在左侧导航栏选择“域名管理”，进入域名管理界面。
3.  单击域名右侧“配置 ”，选择“防盗链配置”页签。
4.  单击“Referer防盗链“。弹出“配置Referer防盗链“页面。
5.  单击“开关“。配置Referer防盗链参数，如[图1 Referer防盗链配置信息](#fig1470581991315)所示。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >当前Referer防盗链配置不支持带端口。

    **图 1**  Referer防盗链配置信息<a name="fig1470581991315"></a>  
    ![](figures/Referer防盗链配置信息.png "Referer防盗链配置信息")

    防盗链配置及对应访问权限说明如[表1](#zh-cn_topic_0129356805_table837817528191)所示。

    **表 1**  参数说明

    <a name="zh-cn_topic_0129356805_table837817528191"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0129356805_zh-cn_topic_0111450891_row19890101885714"><th class="cellrowborder" valign="top" width="10.67%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p182343561940"><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p182343561940"></a><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p182343561940"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="89.33%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p6890181895711"><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p6890181895711"></a><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p6890181895711"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0129356805_zh-cn_topic_0111450891_row1089016185579"><td class="cellrowborder" valign="top" width="10.67%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p323410562417"><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p323410562417"></a><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p323410562417"></a>类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="89.33%" headers="mcps1.2.3.1.2 "><div class="p" id="p4796204561519"><a name="p4796204561519"></a><a name="p4796204561519"></a>支持黑名单和白名单模式。<a name="ul1528259181510"></a><a name="ul1528259181510"></a><ul id="ul1528259181510"><li>Referer黑名单：允许非名单内的域名请求访问媒资，拒绝名单中的域名请求访问。</li><li>Referer白名单：允许名单内的域名请求访问点播媒资，拒绝其它域名请求访问。</li></ul>
    </div>
    <div class="p" id="p5232182113217"><a name="p5232182113217"></a><a name="p5232182113217"></a>包含空Referer是指HTTP请求Header中的Referer内容为空，或者无Referer。根据选择的黑名单或白名单，勾选“包含空Referer”的效果是不同的。<a name="ul413616772312"></a><a name="ul413616772312"></a><ul id="ul413616772312"><li>黑名单模式：勾选“包含空Referer”表示若请求中的Referer为空，则拒绝该请求，否则允许。</li><li>白名单模式：勾选“包含空Referer”表示若请求中的Referer为空，则允许该请求，否则拒绝。</li></ul>
    </div>
    </td>
    </tr>
    <tr id="zh-cn_topic_0129356805_zh-cn_topic_0111450891_row4725335657"><td class="cellrowborder" valign="top" width="10.67%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p1872653520517"><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p1872653520517"></a><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p1872653520517"></a>规则</p>
    </td>
    <td class="cellrowborder" valign="top" width="89.33%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p15426936145216"><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p15426936145216"></a><a name="zh-cn_topic_0129356805_zh-cn_topic_0111450891_p15426936145216"></a>黑名单或白名单中的域名。</p>
    <p id="p1863020169579"><a name="p1863020169579"></a><a name="p1863020169579"></a>支持输入域名或IP地址，以英文“;”进行分割，域名、IP地址可混合输入，支持泛域名添加。输入的域名、IP地址总数不能超过100个。</p>
    <p id="p20551112435715"><a name="p20551112435715"></a><a name="p20551112435715"></a>示例如下：</p>
    <pre class="screen" id="screen1657983116576"><a name="screen1657983116576"></a><a name="screen1657983116576"></a>www.example.com;*.test.com;192.168.0.0</pre>
    </td>
    </tr>
    </tbody>
    </table>

6.  配置完成后，单击“确定“。

    大约需要3-5分钟，Referer防盗链才生效。


