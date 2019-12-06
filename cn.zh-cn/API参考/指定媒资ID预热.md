# 指定媒资ID预热<a name="ZH-CN_TOPIC_0145105867"></a>

## 功能描述<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section114814192538"></a>

媒资发布后，可通过指定媒资ID向CDN预热。用户初次请求时，将由CDN节点提供内容分发，加快用户下载缓存时间，提高用户体验。

## 请求URI<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section5241024145313"></a>

POST /v1.0/\{[project\_id](获取项目ID.md)\}/asset/preheating

## 请求参数<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section7297229175319"></a>

**表 1**  请求参数

<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_table48653720"></a>
<table><thead align="left"><tr id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_row50698484"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p12936535"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p12936535"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p12936535"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p51005947"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p51005947"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p51005947"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p41226423"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p41226423"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p41226423"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="p17826727917"><a name="p17826727917"></a><a name="p17826727917"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_row4372186"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p18602825"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p18602825"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p18602825"></a>asset_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p49225929"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p49225929"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p49225929"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p30433889"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p30433889"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p30433889"></a>发布后媒资ID</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p5234344393"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p5234344393"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p5234344393"></a>M</p>
</td>
</tr>
</tbody>
</table>

## 请求样例<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section1249493515311"></a>

```
{
   "asset_id": "f488337c31c8e4622f1590735b134c65"  
}
```

## 返回参数<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section162761640105314"></a>

-   **处理成功时返回无返回参数**
-   **处理失败时返回**

    **表 2**  处理失败返回参数

    <a name="table64701053171711"></a>
    <table><thead align="left"><tr id="row5469115311175"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p94691753151720"><a name="p94691753151720"></a><a name="p94691753151720"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p946995391713"><a name="p946995391713"></a><a name="p946995391713"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p154691353151718"><a name="p154691353151718"></a><a name="p154691353151718"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1047017536178"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p346945311172"><a name="p346945311172"></a><a name="p346945311172"></a>error_code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p2470653141714"><a name="p2470653141714"></a><a name="p2470653141714"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p7470653151719"><a name="p7470653151719"></a><a name="p7470653151719"></a>错误码。</p>
    </td>
    </tr>
    <tr id="row64702053141720"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p9470155318174"><a name="p9470155318174"></a><a name="p9470155318174"></a>error_msg</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p347010539174"><a name="p347010539174"></a><a name="p347010539174"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1047085391712"><a name="p1047085391712"></a><a name="p1047085391712"></a>错误描述。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 返回样例<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section1164111461532"></a>

-   处理成功返回（202 Accepted）
-   处理失败返回（400 Bad Request\)

    ```
     
    {
      "error_code": "VOD.10053",
      "error_msg": "请求参数非法，非法字段：{xx}。"
    }
    ```


## 错误码<a name="section569214377267"></a>

错误码请参见[错误码](错误码.md)。

