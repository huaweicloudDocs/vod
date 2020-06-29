# 查询TopN媒资信息<a name="vod_04_0105"></a>

## 功能介绍<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_section114814192538"></a>

查询指定域名在指定日期播放次数排名Top 100的媒资统计数据。

## 调试<a name="section16406630174316"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=VOD&api=queryTopStatistics)中直接运行调试该接口。

## URI<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_section5241024145313"></a>

GET /v1.0/\{[project\_id](获取项目ID.md)\}/asset/top-statistics

**表 1**  路径参数

<a name="table6869913124919"></a>
<table><thead align="left"><tr id="vod_04_0196_row58691013184917"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="vod_04_0196_p18869171324920"><a name="vod_04_0196_p18869171324920"></a><a name="vod_04_0196_p18869171324920"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="vod_04_0196_p1386920134497"><a name="vod_04_0196_p1386920134497"></a><a name="vod_04_0196_p1386920134497"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="vod_04_0196_p1386931394910"><a name="vod_04_0196_p1386931394910"></a><a name="vod_04_0196_p1386931394910"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="vod_04_0196_p10869213144912"><a name="vod_04_0196_p10869213144912"></a><a name="vod_04_0196_p10869213144912"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="vod_04_0196_row1586931374911"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p14253192105011"><a name="vod_04_0196_p14253192105011"></a><a name="vod_04_0196_p14253192105011"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p62548235018"><a name="vod_04_0196_p62548235018"></a><a name="vod_04_0196_p62548235018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p0254323500"><a name="vod_04_0196_p0254323500"></a><a name="vod_04_0196_p0254323500"></a>项目ID，获取方法请参考<a href="https://support.huaweicloud.com/usermanual-vod/vod_01_0058.html" target="_blank" rel="noopener noreferrer">获取项目ID</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p9936171618529"><a name="vod_04_0196_p9936171618529"></a><a name="vod_04_0196_p9936171618529"></a>M</p>
</td>
</tr>
</tbody>
</table>

**表 2** Query参数

<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_table19206131"></a>
<table><thead align="left"><tr id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_row16057184"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25563541"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25563541"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25563541"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p17343428"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p17343428"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p17343428"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p57380926"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p57380926"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p57380926"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="p9242121093813"><a name="p9242121093813"></a><a name="p9242121093813"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_row30822828"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p13621136"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p13621136"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p13621136"></a>domain</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46380963"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46380963"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46380963"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p8361154813166"><a name="p8361154813166"></a><a name="p8361154813166"></a>TopN媒资信息要么查询单个域名要么查询所有域名。</p>
<p id="p127871167428"><a name="p127871167428"></a><a name="p127871167428"></a>取值如下：</p>
<a name="ul11782191634215"></a><a name="ul11782191634215"></a><ul id="ul11782191634215"><li>单个加速域名，格式：example.test1.com。</li><li>ALL：表示查询名下全部域名。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33910007"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33910007"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33910007"></a>M</p>
</td>
</tr>
<tr id="row751454883517"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p14531204803520"><a name="p14531204803520"></a><a name="p14531204803520"></a>date</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p13531104818354"><a name="p13531104818354"></a><a name="p13531104818354"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p1854632163617"><a name="p1854632163617"></a><a name="p1854632163617"></a>查询日期，格式为yyyymmdd。</p>
<a name="ul20962449184219"></a><a name="ul20962449184219"></a><ul id="ul20962449184219"><li>date必须为昨天或之前的日期。</li><li>最多只能查最近一个月内的数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p1953144833518"><a name="p1953144833518"></a><a name="p1953144833518"></a>M</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_section7297229175319"></a>

**表 3**  请求Header参数

<a name="HeaderParameter"></a>
<table><thead align="left"><tr id="vod_04_0196_row1359311223199"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="vod_04_0196_p959302213191"><a name="vod_04_0196_p959302213191"></a><a name="vod_04_0196_p959302213191"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="vod_04_0196_p6594132291914"><a name="vod_04_0196_p6594132291914"></a><a name="vod_04_0196_p6594132291914"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="vod_04_0196_p1659492213198"><a name="vod_04_0196_p1659492213198"></a><a name="vod_04_0196_p1659492213198"></a>描述</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="vod_04_0196_p971659181911"><a name="vod_04_0196_p971659181911"></a><a name="vod_04_0196_p971659181911"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="vod_04_0196_row5593132218192"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p959417226199"><a name="vod_04_0196_p959417226199"></a><a name="vod_04_0196_p959417226199"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p5594132231911"><a name="vod_04_0196_p5594132231911"></a><a name="vod_04_0196_p5594132231911"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p1159416229196"><a name="vod_04_0196_p1159416229196"></a><a name="vod_04_0196_p1159416229196"></a>用户Token。 通过调用IAM服务获取用户Token接口获取（响应消息头中X-Subject-Token的值）。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p147114598193"><a name="vod_04_0196_p147114598193"></a><a name="vod_04_0196_p147114598193"></a>M</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_section1249493515311"></a>

```
GET /v1.0/{project_id}/asset/top-statistics?domain=ALL&date=20190612
```

## 返回参数<a name="section12889132584818"></a>

-   **处理成功时返回**

    **表 4**  处理成功返回参数

    <a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_table17829578"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_row36608226"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p12476353"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p12476353"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p12476353"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p51649700"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p51649700"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p51649700"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p3951668"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p3951668"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p3951668"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_row33716833"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46708959"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46708959"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46708959"></a>top_urls</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p38413446"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p38413446"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p38413446"></a>Array of <a href="#table114221659173917">TopUrl </a>objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25329374"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25329374"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25329374"></a>统计结果数组，最多返回100个结果。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 5**  TopUrl参数说明

    <a name="table114221659173917"></a>
    <table><thead align="left"><tr id="row1242215943913"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1042212597391"><a name="p1042212597391"></a><a name="p1042212597391"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p13439159133918"><a name="p13439159133918"></a><a name="p13439159133918"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p11422155983913"><a name="p11422155983913"></a><a name="p11422155983913"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row74397599397"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p5439559163920"><a name="p5439559163920"></a><a name="p5439559163920"></a>asset_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1439195911398"><a name="p1439195911398"></a><a name="p1439195911398"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p10439859103913"><a name="p10439859103913"></a><a name="p10439859103913"></a>媒资ID。</p>
    </td>
    </tr>
    <tr id="row1072004164013"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p47202424018"><a name="p47202424018"></a><a name="p47202424018"></a>value</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1172004174019"><a name="p1172004174019"></a><a name="p1172004174019"></a><span id="ph167394921810"><a name="ph167394921810"></a><a name="ph167394921810"></a>Long</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p672012412407"><a name="p672012412407"></a><a name="p672012412407"></a>总播放次数。</p>
    </td>
    </tr>
    <tr id="row1650179204019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p4675712413"><a name="p4675712413"></a><a name="p4675712413"></a>title</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p050112984013"><a name="p050112984013"></a><a name="p050112984013"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p14501199114013"><a name="p14501199114013"></a><a name="p14501199114013"></a>媒资名称。</p>
    </td>
    </tr>
    <tr id="row18876131311403"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p158761613144015"><a name="p158761613144015"></a><a name="p158761613144015"></a>duration</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p18761131406"><a name="p18761131406"></a><a name="p18761131406"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p755917496194"><a name="p755917496194"></a><a name="p755917496194"></a>媒资时长。</p>
    <p id="p158761913114013"><a name="p158761913114013"></a><a name="p158761913114013"></a>单位：秒。</p>
    </td>
    </tr>
    <tr id="row2511425154015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1351142584011"><a name="p1351142584011"></a><a name="p1351142584011"></a>size</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p35122584014"><a name="p35122584014"></a><a name="p35122584014"></a><span id="ph843414461810"><a name="ph843414461810"></a><a name="ph843414461810"></a>Long</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p8707165501913"><a name="p8707165501913"></a><a name="p8707165501913"></a>媒资原始大小。</p>
    <p id="p651142518402"><a name="p651142518402"></a><a name="p651142518402"></a>单位：字节。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   **处理失败时返回**

    **表 6**  处理失败返回参数

    <a name="table8107146194412"></a>
    <table><thead align="left"><tr id="row16107862441"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1412466124414"><a name="p1412466124414"></a><a name="p1412466124414"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p121241568444"><a name="p121241568444"></a><a name="p121241568444"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1312414674420"><a name="p1312414674420"></a><a name="p1312414674420"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row13124116124413"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p11240634415"><a name="p11240634415"></a><a name="p11240634415"></a>error_code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p414018615446"><a name="p414018615446"></a><a name="p414018615446"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p161241669445"><a name="p161241669445"></a><a name="p161241669445"></a>错误码。</p>
    </td>
    </tr>
    <tr id="row01401168446"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p171409604412"><a name="p171409604412"></a><a name="p171409604412"></a>error_msg</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p91404614444"><a name="p91404614444"></a><a name="p91404614444"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p16140666447"><a name="p16140666447"></a><a name="p16140666447"></a>错误描述。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 返回示例<a name="section5664343618"></a>

-   处理成功时返回（200 OK）

    ```
    {   
        "top_urls": 
        [     
         { 
              "value": 0, 
              "asset_id": "548b6023bf2cc925bd64343f04ca0f88",
    	  "title": "test",
    	  "duration": 0,
    	  "size": 0
    	  }
    	]
    }
    ```


-   处理失败时返回 （400 Bad Request）

    ```
    {
      "error_code": "VOD.10053",
      "error_msg": "请求参数非法，非法字段：{xx}。"
    }
    ```


## 错误码<a name="section569214377267"></a>

错误码请参见[错误码](错误码.md)。

