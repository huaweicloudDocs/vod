# 查询CDN统计信息<a name="vod_04_0103"></a>

## 功能描述<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_section114814192538"></a>

查询CDN的统计数据，包括流量、峰值带宽、请求总数、请求命中率、流量命中率。

## 请求URI<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_section5241024145313"></a>

GET /v1.0/\{[project\_id](获取项目ID.md)\}/asset/cdn-statistics

## 请求参数<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_section7297229175319"></a>

**表 1**  请求参数

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
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p129571139515"><a name="p129571139515"></a><a name="p129571139515"></a>域名列表，多个域名以逗号（半角）分隔。</p>
<p id="p133714813111"><a name="p133714813111"></a><a name="p133714813111"></a>示例：example.test1.com,example.test2.com。</p>
<p id="p1312433710114"><a name="p1312433710114"></a><a name="p1312433710114"></a>ALL表示查询名下全部域名。一次最多查询100个域名。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33910007"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33910007"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33910007"></a>M</p>
</td>
</tr>
<tr id="row54433417271"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p344317410270"><a name="p344317410270"></a><a name="p344317410270"></a>start_time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p154436415278"><a name="p154436415278"></a><a name="p154436415278"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p1942152703214"><a name="p1942152703214"></a><a name="p1942152703214"></a>起始时间，格式为yyyymmddhhmmss。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p144315442717"><a name="p144315442717"></a><a name="p144315442717"></a>O</p>
</td>
</tr>
<tr id="row18841213122719"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p784171362715"><a name="p784171362715"></a><a name="p784171362715"></a>end_time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p284171392716"><a name="p284171392716"></a><a name="p284171392716"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p1512020576313"><a name="p1512020576313"></a><a name="p1512020576313"></a>结束时间，格式为yyyymmddhhmmss。</p>
<a name="ul172315577384"></a><a name="ul172315577384"></a><ul id="ul172315577384"><li><span class="parmname" id="parmname1991695919118"><a name="parmname1991695919118"></a><a name="parmname1991695919118"></a>“start_time”</span>、<span class="parmname" id="parmname131791224211"><a name="parmname131791224211"></a><a name="parmname131791224211"></a>“end_time”</span>均不存在时，<span class="parmname" id="parmname19556941216"><a name="parmname19556941216"></a><a name="parmname19556941216"></a>“start_time”</span>取当天零点，<span class="parmname" id="parmname62902719216"><a name="parmname62902719216"></a><a name="parmname62902719216"></a>“end_time”</span>取当前时间。</li><li><span class="parmname" id="parmname13851392029"><a name="parmname13851392029"></a><a name="parmname13851392029"></a>“start_time”</span>不存在、<span class="parmname" id="parmname940514112216"><a name="parmname940514112216"></a><a name="parmname940514112216"></a>“end_time”</span>存在，请求非法。</li><li><span class="parmname" id="parmname017518177215"><a name="parmname017518177215"></a><a name="parmname017518177215"></a>“start_time”</span>存在、<span class="parmname" id="parmname10925121813219"><a name="parmname10925121813219"></a><a name="parmname10925121813219"></a>“end_time”</span>不存在，<span class="parmname" id="parmname1598511201213"><a name="parmname1598511201213"></a><a name="parmname1598511201213"></a>“end_time”</span>取当前时间。</li><li>只能查询最近三个月内的数据，且时间跨度不能超过31天。</li><li>起始时间和结束时间会自动规整，起始时间规整为指定时间所在的整点时刻，结束时间规整为指定时间所在时间的下一小时整点时刻。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p198411342712"><a name="p198411342712"></a><a name="p198411342712"></a>O</p>
</td>
</tr>
<tr id="row106461117132710"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1264614171273"><a name="p1264614171273"></a><a name="p1264614171273"></a>interval</p>
<p id="p1810718511038"><a name="p1810718511038"></a><a name="p1810718511038"></a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p86460172276"><a name="p86460172276"></a><a name="p86460172276"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p1263164312210"><a name="p1263164312210"></a><a name="p1263164312210"></a>查询粒度间隔。</p>
<p id="p1412154514215"><a name="p1412154514215"></a><a name="p1412154514215"></a>取值如下：</p>
<a name="ul153151021033"></a><a name="ul153151021033"></a><ul id="ul153151021033"><li>时间跨度1天：5分钟、1小时、4小时、8小时，分别对应300秒、3600秒、14400秒和28800秒。</li><li>时间跨度2~7天：1小时、4小时、8小时、1天，分别对应3600秒、14400秒、28800秒和86400秒。</li><li>时间跨度8~31天：4小时、8小时、1天，分别对应14400秒、28800秒和86400秒。</li></ul>
<p id="p135908145312"><a name="p135908145312"></a><a name="p135908145312"></a>单位：秒。</p>
<p id="p1877197183018"><a name="p1877197183018"></a><a name="p1877197183018"></a>若不设置，默认取对应时间跨度的最小间隔。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p364671772717"><a name="p364671772717"></a><a name="p364671772717"></a>O</p>
</td>
</tr>
<tr id="row7396182812271"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p103968288276"><a name="p103968288276"></a><a name="p103968288276"></a>stat_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p839611281272"><a name="p839611281272"></a><a name="p839611281272"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p21850322317"><a name="p21850322317"></a><a name="p21850322317"></a>统计数据类型。</p>
<div class="p" id="p870861917309"><a name="p870861917309"></a><a name="p870861917309"></a>取值如下：<a name="ul946271184020"></a><a name="ul946271184020"></a><ul id="ul946271184020"><li>cdn_bw：CDN峰值带宽</li><li>cdn_flux：CDN流量</li><li>req_num：请求总数</li><li>req_hit_rate：请求命中率</li><li>flux_hit_rate：流量命中率</li></ul>
</div>
<p id="p1696816561538"><a name="p1696816561538"></a><a name="p1696816561538"></a>每次只能查询一种统计数据。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p20396142842711"><a name="p20396142842711"></a><a name="p20396142842711"></a>M</p>
</td>
</tr>
</tbody>
</table>

## 请求样例<a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_section1249493515311"></a>

```
GET /v1.0/{project_id}/asset/cdn-statistics?domain=www.example.com&stat_type=cdn_bw
```

## 返回参数<a name="section12889132584818"></a>

-   **处理成功时返回**

    **表 2**  处理成功返回参数

    <a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_table17829578"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_row36608226"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p12476353"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p12476353"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p12476353"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p51649700"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p51649700"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p51649700"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p3951668"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p3951668"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p3951668"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_row33716833"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46708959"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46708959"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46708959"></a>start_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p38413446"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p38413446"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p38413446"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25329374"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25329374"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p25329374"></a>统计起始时间。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_row63096163"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p10515579"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p10515579"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p10515579"></a>interval</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p4805945"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p4805945"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p4805945"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46455584"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46455584"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p46455584"></a>统计间隔。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_row49997107"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p151751827134011"><a name="p151751827134011"></a><a name="p151751827134011"></a>values</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33200472"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33200472"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p33200472"></a>Array of integers</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1344781221020"><a name="p1344781221020"></a><a name="p1344781221020"></a>采样数据数组。</p>
    <p id="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p2895395"><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p2895395"></a><a name="zh-cn_topic_0128109924_zh-cn_topic_0127930889_p2895395"></a>从start_time开始，每个间隔对应一个采样数据。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   **处理失败时返回**

    **表 3**  处理失败返回参数

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


## 返回样例<a name="section1879952173615"></a>

-   处理成功返回 （200 OK）

    ```
    {   
         "start_time": "string",   
         "interval": 0,  
         "values": [0] 
    }
    ```


-   处理失败返回 （400 Bad Request）

    ```
    {
      "error_code": "VOD.10053",
      "error_msg": "请求参数非法，非法字段：{xx}。"
    }
    ```


## 错误码<a name="section569214377267"></a>

错误码请参见[错误码](错误码.md)。

