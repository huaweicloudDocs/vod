# 配置CNAME（非华为云）<a name="common00002"></a>

通过在DNS服务商处配置CNAME记录，将加速域名以CNAME方式指向CDN服务中对应的CNAME域名，域名解析生效后，该域名的所有请求都将转向CDN节点。

## 注意事项<a name="section19392323123412"></a>

-   请前往您的域名解析服务商处配置CNAME记录，具体操作请咨询您的域名解析服务提供商。
-   以下以在万网、DNSPod、新网配置CNAME域名解析为例，操作步骤仅供参考。如与实际配置不符，请以各自DNS服务商的信息为准。

## DNSPod配置方法<a name="zh-cn_topic_0117188957_section94001837173913"></a>

若您的DNS服务商为DNSPod，您可通过如下步骤配置CNAME记录。

1.  登录DNSPod控制台。
2.  在左侧菜单栏中，选择“域名解析“。
3.  在待添加记录集的域名所在行，单击相应域名。
4.  单击“添加记录“，弹出“添加记录“页面。
5.  根据界面提示填写参数配置，参数信息如[表1](#zh-cn_topic_0117188957_table4339246163017)所示。

    **表 1**  参数说明

    <a name="zh-cn_topic_0117188957_table4339246163017"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0117188957_row1850614610304"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0117188957_p4506146113017"><a name="zh-cn_topic_0117188957_p4506146113017"></a><a name="zh-cn_topic_0117188957_p4506146113017"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0117188957_p250684663016"><a name="zh-cn_topic_0117188957_p250684663016"></a><a name="zh-cn_topic_0117188957_p250684663016"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0117188957_p650617464300"><a name="zh-cn_topic_0117188957_p650617464300"></a><a name="zh-cn_topic_0117188957_p650617464300"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0117188957_row13507124633012"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p1750704620309"><a name="zh-cn_topic_0117188957_p1750704620309"></a><a name="zh-cn_topic_0117188957_p1750704620309"></a>主机记录</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p185071046183018"><a name="zh-cn_topic_0117188957_p185071046183018"></a><a name="zh-cn_topic_0117188957_p185071046183018"></a>主机记录指域名前缀。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p1950744620308"><a name="zh-cn_topic_0117188957_p1950744620308"></a><a name="zh-cn_topic_0117188957_p1950744620308"></a>example</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row15507194610301"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p2050764610303"><a name="zh-cn_topic_0117188957_p2050764610303"></a><a name="zh-cn_topic_0117188957_p2050764610303"></a>记录类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p8507346113013"><a name="zh-cn_topic_0117188957_p8507346113013"></a><a name="zh-cn_topic_0117188957_p8507346113013"></a>记录集的类型，此处为CNAME类型。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p1507164611304"><a name="zh-cn_topic_0117188957_p1507164611304"></a><a name="zh-cn_topic_0117188957_p1507164611304"></a>CNAME-Canonical name</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row16507124618308"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p10507546113020"><a name="zh-cn_topic_0117188957_p10507546113020"></a><a name="zh-cn_topic_0117188957_p10507546113020"></a>线路类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p4507174611306"><a name="zh-cn_topic_0117188957_p4507174611306"></a><a name="zh-cn_topic_0117188957_p4507174611306"></a>一般情况下，若空间商只提供了一个IP地址或域名，选择「默认」即可。其他特殊情况请咨询您的DNS服务商。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p1850784643012"><a name="zh-cn_topic_0117188957_p1850784643012"></a><a name="zh-cn_topic_0117188957_p1850784643012"></a>默认</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row15078461308"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p3507194610305"><a name="zh-cn_topic_0117188957_p3507194610305"></a><a name="zh-cn_topic_0117188957_p3507194610305"></a>记录值</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p175071646133010"><a name="zh-cn_topic_0117188957_p175071646133010"></a><a name="zh-cn_topic_0117188957_p175071646133010"></a>需指向的域名，即CDN为您分配的CNAME域名。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p145078463308"><a name="zh-cn_topic_0117188957_p145078463308"></a><a name="zh-cn_topic_0117188957_p145078463308"></a>example.test.com.c.cdnhwc1.com</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row10507946103013"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p115071346143010"><a name="zh-cn_topic_0117188957_p115071346143010"></a><a name="zh-cn_topic_0117188957_p115071346143010"></a>权重</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p150734683017"><a name="zh-cn_topic_0117188957_p150734683017"></a><a name="zh-cn_topic_0117188957_p150734683017"></a>无需填写。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p450714616301"><a name="zh-cn_topic_0117188957_p450714616301"></a><a name="zh-cn_topic_0117188957_p450714616301"></a>-</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row7507154603015"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p45081446103014"><a name="zh-cn_topic_0117188957_p45081446103014"></a><a name="zh-cn_topic_0117188957_p45081446103014"></a>MX优先级</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p75081346163013"><a name="zh-cn_topic_0117188957_p75081346163013"></a><a name="zh-cn_topic_0117188957_p75081346163013"></a>无需填写。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p1650819461301"><a name="zh-cn_topic_0117188957_p1650819461301"></a><a name="zh-cn_topic_0117188957_p1650819461301"></a>-</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row0508204673011"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p125081946123017"><a name="zh-cn_topic_0117188957_p125081946123017"></a><a name="zh-cn_topic_0117188957_p125081946123017"></a>TTL(秒)</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p17508164613303"><a name="zh-cn_topic_0117188957_p17508164613303"></a><a name="zh-cn_topic_0117188957_p17508164613303"></a>记录集的有效缓存时间，以秒为单位。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p12508114612306"><a name="zh-cn_topic_0117188957_p12508114612306"></a><a name="zh-cn_topic_0117188957_p12508114612306"></a>保持默认即可。</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“保存“，完成添加。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >CNAME记录添加完成后实时生效。


## 万网配置方法<a name="zh-cn_topic_0117188957_section7421940184219"></a>

若您的DNS服务商为万网，您可通过如下步骤配置CNAME记录。

1.  登录万网管理控制台。
2.  在主导航栏中，选择“产品与服务 \> 云解析“，进入云解析服务页面。
3.  在待添加记录集的域名所在行，单击相应域名。
4.  单击“添加解析“，弹出“添加解析“页面。
5.  根据界面提示填写参数配置，参数信息如[表2](#zh-cn_topic_0117188957_table3565182004512)所示。

    **表 2**  参数说明

    <a name="zh-cn_topic_0117188957_table3565182004512"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0117188957_row11730162017456"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p1829714120342"><a name="p1829714120342"></a><a name="p1829714120342"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p182975419343"><a name="p182975419343"></a><a name="p182975419343"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0117188957_p5730320164517"><a name="zh-cn_topic_0117188957_p5730320164517"></a><a name="zh-cn_topic_0117188957_p5730320164517"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0117188957_row473032034512"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p87311720134511"><a name="zh-cn_topic_0117188957_p87311720134511"></a><a name="zh-cn_topic_0117188957_p87311720134511"></a>记录类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p473172010459"><a name="zh-cn_topic_0117188957_p473172010459"></a><a name="zh-cn_topic_0117188957_p473172010459"></a>记录集的类型，此处为CNAME类型。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p187311420184518"><a name="zh-cn_topic_0117188957_p187311420184518"></a><a name="zh-cn_topic_0117188957_p187311420184518"></a>CNAME-Canonical name</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row8731102014519"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p1773117208459"><a name="zh-cn_topic_0117188957_p1773117208459"></a><a name="zh-cn_topic_0117188957_p1773117208459"></a>主机记录</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p147311120194514"><a name="zh-cn_topic_0117188957_p147311120194514"></a><a name="zh-cn_topic_0117188957_p147311120194514"></a>主机记录指域名前缀。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p973182024511"><a name="zh-cn_topic_0117188957_p973182024511"></a><a name="zh-cn_topic_0117188957_p973182024511"></a>example</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row4731162054515"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p117311020104519"><a name="zh-cn_topic_0117188957_p117311020104519"></a><a name="zh-cn_topic_0117188957_p117311020104519"></a>解析线路</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p17731122064519"><a name="zh-cn_topic_0117188957_p17731122064519"></a><a name="zh-cn_topic_0117188957_p17731122064519"></a>保持默认即可。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p97312020114515"><a name="zh-cn_topic_0117188957_p97312020114515"></a><a name="zh-cn_topic_0117188957_p97312020114515"></a>默认</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row1731202017455"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p373122094513"><a name="zh-cn_topic_0117188957_p373122094513"></a><a name="zh-cn_topic_0117188957_p373122094513"></a>记录值</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p19731162011458"><a name="zh-cn_topic_0117188957_p19731162011458"></a><a name="zh-cn_topic_0117188957_p19731162011458"></a>需指向的域名，即CDN为您分配的CNAME域名。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p5731620114514"><a name="zh-cn_topic_0117188957_p5731620114514"></a><a name="zh-cn_topic_0117188957_p5731620114514"></a>example.test.com.c.cdnhwc1.com</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row1273112020452"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p27311720194516"><a name="zh-cn_topic_0117188957_p27311720194516"></a><a name="zh-cn_topic_0117188957_p27311720194516"></a>TTL(秒)</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p57311120114512"><a name="zh-cn_topic_0117188957_p57311120114512"></a><a name="zh-cn_topic_0117188957_p57311120114512"></a>记录集的有效缓存时间，以秒为单位。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p13731112019455"><a name="zh-cn_topic_0117188957_p13731112019455"></a><a name="zh-cn_topic_0117188957_p13731112019455"></a>保持默认</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“确认“，完成添加。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >CNAME记录添加完成后实时生效。


## 新网配置方法<a name="zh-cn_topic_0117188957_section1569151716326"></a>

若您的DNS服务商为新网，您可通过如下步骤添加CNAME记录。

1.  登录新网域名自助管理平台。
2.  选择“域名管理“，进入DNS解析记录管理页面。
3.  选择待添加记录的域名，进入DNS解析记录页面。
4.  根据界面提示填写参数配置，参数信息如[表3](#zh-cn_topic_0117188957_table135101549133312)所示。

    **表 3**  参数说明

    <a name="zh-cn_topic_0117188957_table135101549133312"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0117188957_row17511249163317"><th class="cellrowborder" valign="top" width="15%" id="mcps1.2.4.1.1"><p id="p144866478342"><a name="p144866478342"></a><a name="p144866478342"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="52%" id="mcps1.2.4.1.2"><p id="p34861247143417"><a name="p34861247143417"></a><a name="p34861247143417"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0117188957_p1451184903315"><a name="zh-cn_topic_0117188957_p1451184903315"></a><a name="zh-cn_topic_0117188957_p1451184903315"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0117188957_row951117492335"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p4512349163310"><a name="zh-cn_topic_0117188957_p4512349163310"></a><a name="zh-cn_topic_0117188957_p4512349163310"></a>别名</p>
    </td>
    <td class="cellrowborder" valign="top" width="52%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p4512164913310"><a name="zh-cn_topic_0117188957_p4512164913310"></a><a name="zh-cn_topic_0117188957_p4512164913310"></a>需指向的域名，即CDN为您分配的CNAME域名。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p185121849123316"><a name="zh-cn_topic_0117188957_p185121849123316"></a><a name="zh-cn_topic_0117188957_p185121849123316"></a>example.test.com.c.cdnhwc1.com</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row2512349173315"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p195126495336"><a name="zh-cn_topic_0117188957_p195126495336"></a><a name="zh-cn_topic_0117188957_p195126495336"></a>别名主机</p>
    </td>
    <td class="cellrowborder" valign="top" width="52%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p1651244973314"><a name="zh-cn_topic_0117188957_p1651244973314"></a><a name="zh-cn_topic_0117188957_p1651244973314"></a>表示域名前缀。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p1151219491334"><a name="zh-cn_topic_0117188957_p1151219491334"></a><a name="zh-cn_topic_0117188957_p1151219491334"></a>example</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0117188957_row451254918330"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0117188957_p651614919338"><a name="zh-cn_topic_0117188957_p651614919338"></a><a name="zh-cn_topic_0117188957_p651614919338"></a>TTL（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="52%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0117188957_p19516124917331"><a name="zh-cn_topic_0117188957_p19516124917331"></a><a name="zh-cn_topic_0117188957_p19516124917331"></a>记录集的有效缓存时间，以秒为单位。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0117188957_p1551664917338"><a name="zh-cn_topic_0117188957_p1551664917338"></a><a name="zh-cn_topic_0117188957_p1551664917338"></a>保持默认</p>
    </td>
    </tr>
    </tbody>
    </table>

5.  单击“确认“，完成添加。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >CNAME记录添加完成后实时生效。


## 验证加速域名是否CNAME配置成功<a name="zh-cn_topic_0117188957_section17479726161813"></a>

配置CNAME后，不同的DNS服务商CNAME生效的时间也不同，您可以通过以下方式验证CNAME是否生效。

打开Windows操作系统中的cmd程序，输入如下指令：

```
nslookup -qt=cname 加速域名
```

如果回显CNAME，则表示CNAME配置已经生效。

