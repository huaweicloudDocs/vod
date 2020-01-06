# 指定URL预热<a name="vod_04_0119"></a>

## 功能描述<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section114814192538"></a>

媒资发布后，可通过指定媒资URL向CDN预热。用户初次请求时，将由CDN节点提供内容分发，加快用户下载缓存时间，提高用户体验。

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
<tbody><tr id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_row4372186"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p18602825"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p18602825"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p18602825"></a>urls</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p49225929"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p49225929"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p49225929"></a>Array&nbsp;of&nbsp;strings</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p30433889"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p30433889"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p30433889"></a>发布后媒资URL列表，一次最多只能预热10个URL。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p5234344393"><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p5234344393"></a><a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_p5234344393"></a>M</p>
</td>
</tr>
</tbody>
</table>

## 请求样例<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section1249493515311"></a>

```
{
"urls": [                
   "https://example.com/asset/9db42f5e08c15edecd99a98da241994a/313bfd52a75f95ff48e8bf02eca2ab20.flv",
   "https://example.com/asset/9e455adb02295aa123809e8dc7ca51c1/68b1241af3bf58bcde9914626e07f5af.mp4",
   "https://example.com/asset/9e455adb02295aa123809e8dc7ca51c1/play_video/68b1241af3bf58bcde9914626e07f5af_H.264_480X270_HEAACV1_300.mp4"
]  
}
```

## 返回参数<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section162761640105314"></a>

-   **处理成功时返回**

    **表 2**  处理成功返回参数

    <a name="table264515405256"></a>
    <table><thead align="left"><tr id="row126457406259"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p11645194042512"><a name="p11645194042512"></a><a name="p11645194042512"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p9645194002519"><a name="p9645194002519"></a><a name="p9645194002519"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p564574052514"><a name="p564574052514"></a><a name="p564574052514"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1266064019252"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p20660144092516"><a name="p20660144092516"></a><a name="p20660144092516"></a>task_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p10660124082518"><a name="p10660124082518"></a><a name="p10660124082518"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p196601409252"><a name="p196601409252"></a><a name="p196601409252"></a>预热任务ID。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   **处理失败时返回**

    **表 3**  处理失败返回参数

    <a name="table1568512134916"></a>
    <table><thead align="left"><tr id="row1768510120494"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p668510120495"><a name="p668510120495"></a><a name="p668510120495"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p156851913497"><a name="p156851913497"></a><a name="p156851913497"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1868512117498"><a name="p1868512117498"></a><a name="p1868512117498"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15685117493"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1468510184917"><a name="p1468510184917"></a><a name="p1468510184917"></a>error_code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p56859119495"><a name="p56859119495"></a><a name="p56859119495"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p56858104915"><a name="p56858104915"></a><a name="p56858104915"></a>错误码。</p>
    </td>
    </tr>
    <tr id="row468514116490"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p66851516493"><a name="p66851516493"></a><a name="p66851516493"></a>error_msg</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p15685121104915"><a name="p15685121104915"></a><a name="p15685121104915"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p568515114910"><a name="p568515114910"></a><a name="p568515114910"></a>错误描述。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 返回样例<a name="zh-cn_topic_0128109936_zh-cn_topic_0127939729_section1164111461532"></a>

-   处理成功返回（202 Accepted）

    ```
    {
       "task_id": "5199337c31c8e4622f1590735b13a263"  
    }
    ```

-   处理失败返回（400 Bad Request\)

    ```
     
    {
      "error_code": "VOD.10053",
      "error_msg": "请求参数非法，非法字段：{xx}。"
    }
    ```


## 错误码<a name="section569214377267"></a>

错误码请参见[错误码](错误码.md)。

