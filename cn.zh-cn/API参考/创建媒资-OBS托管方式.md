# 创建媒资：OBS托管方式<a name="vod_04_0051"></a>

## 功能介绍<a name="section11101332175018"></a>

通过存量托管的方式，将已存储在OBS桶中的音视频文件同步到点播服务。

OBS托管方式分为增量托管和存量托管，增量托管暂只支持通过视频点播控制台配置，配置后，若OBS有新增音视频文件，则会自动同步到点播服务中，具体请参见[增量托管](https://support.huaweicloud.com/usermanual-vod/vod010032.html)。两个托管方式都需要先将对应的OBS桶授权给点播服务，具体请参见[桶授权](https://support.huaweicloud.com/usermanual-vod/vod010031.html)。

## 调试<a name="section189092186114"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=VOD&api=CreateTakeOverTask)中直接运行调试该接口。

## URI<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section5627230172812"></a>

POST /v1.0/\{[project\_id](获取项目ID.md)\}/asset/obs/host/stock/task

**表 1**  路径参数

<a name="table6869913124919"></a>
<table><thead align="left"><tr id="vod_04_0196_row58691013184917"><th class="cellrowborder" valign="top" width="18.98%" id="mcps1.2.5.1.1"><p id="vod_04_0196_p18869171324920"><a name="vod_04_0196_p18869171324920"></a><a name="vod_04_0196_p18869171324920"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.400000000000002%" id="mcps1.2.5.1.2"><p id="vod_04_0196_p16174217193312"><a name="vod_04_0196_p16174217193312"></a><a name="vod_04_0196_p16174217193312"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.299999999999997%" id="mcps1.2.5.1.3"><p id="vod_04_0196_p1386920134497"><a name="vod_04_0196_p1386920134497"></a><a name="vod_04_0196_p1386920134497"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.32%" id="mcps1.2.5.1.4"><p id="vod_04_0196_p1386931394910"><a name="vod_04_0196_p1386931394910"></a><a name="vod_04_0196_p1386931394910"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="vod_04_0196_row1586931374911"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p14253192105011"><a name="vod_04_0196_p14253192105011"></a><a name="vod_04_0196_p14253192105011"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.400000000000002%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p18172181763318"><a name="vod_04_0196_p18172181763318"></a><a name="vod_04_0196_p18172181763318"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.299999999999997%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p62548235018"><a name="vod_04_0196_p62548235018"></a><a name="vod_04_0196_p62548235018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.32%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p0254323500"><a name="vod_04_0196_p0254323500"></a><a name="vod_04_0196_p0254323500"></a>项目ID，获取方法请参考<a href="https://support.huaweicloud.com/usermanual-vod/vod_01_0058.html" target="_blank" rel="noopener noreferrer">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section13573338112812"></a>

**表 2**  请求Header参数

<a name="HeaderParameter"></a>
<table><thead align="left"><tr id="vod_04_0196_row1359311223199"><th class="cellrowborder" valign="top" width="18.89%" id="mcps1.2.5.1.1"><p id="vod_04_0196_p959302213191"><a name="vod_04_0196_p959302213191"></a><a name="vod_04_0196_p959302213191"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.23%" id="mcps1.2.5.1.2"><p id="vod_04_0196_p10968335203313"><a name="vod_04_0196_p10968335203313"></a><a name="vod_04_0196_p10968335203313"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.04%" id="mcps1.2.5.1.3"><p id="vod_04_0196_p6594132291914"><a name="vod_04_0196_p6594132291914"></a><a name="vod_04_0196_p6594132291914"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.84%" id="mcps1.2.5.1.4"><p id="vod_04_0196_p1659492213198"><a name="vod_04_0196_p1659492213198"></a><a name="vod_04_0196_p1659492213198"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="vod_04_0196_row5593132218192"><td class="cellrowborder" valign="top" width="18.89%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p959417226199"><a name="vod_04_0196_p959417226199"></a><a name="vod_04_0196_p959417226199"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="19.23%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p189688351336"><a name="vod_04_0196_p189688351336"></a><a name="vod_04_0196_p189688351336"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p5594132231911"><a name="vod_04_0196_p5594132231911"></a><a name="vod_04_0196_p5594132231911"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.84%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p1159416229196"><a name="vod_04_0196_p1159416229196"></a><a name="vod_04_0196_p1159416229196"></a>用户Token。 通过调用IAM服务获取用户Token接口获取（响应消息头中X-Subject-Token的值）。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_table11962631"></a>
<table><thead align="left"><tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row4709306"><th class="cellrowborder" valign="top" width="19.1%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p45909486"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p45909486"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p45909486"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.93%" id="mcps1.2.5.1.2"><p id="p152145345012"><a name="p152145345012"></a><a name="p152145345012"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.669999999999998%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27680879"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27680879"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27680879"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.3%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27558692"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27558692"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27558692"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row9016510488"><td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.5.1.1 "><p id="p121127919359"><a name="p121127919359"></a><a name="p121127919359"></a>bucket</p>
</td>
<td class="cellrowborder" valign="top" width="18.93%" headers="mcps1.2.5.1.2 "><p id="p135181653135018"><a name="p135181653135018"></a><a name="p135181653135018"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.5.1.3 "><p id="p9485043195716"><a name="p9485043195716"></a><a name="p9485043195716"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.3%" headers="mcps1.2.5.1.4 "><p id="p1050592203211"><a name="p1050592203211"></a><a name="p1050592203211"></a>源桶名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row14539135243618"><td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.5.1.1 "><p id="p17885131823518"><a name="p17885131823518"></a><a name="p17885131823518"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="18.93%" headers="mcps1.2.5.1.2 "><p id="p55121353155018"><a name="p55121353155018"></a><a name="p55121353155018"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.5.1.3 "><p id="p953131519580"><a name="p953131519580"></a><a name="p953131519580"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.3%" headers="mcps1.2.5.1.4 "><p id="p3503722193214"><a name="p3503722193214"></a><a name="p3503722193214"></a>源目录名或源文件名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row57482668"><td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.5.1.1 "><p id="p20952192314359"><a name="p20952192314359"></a><a name="p20952192314359"></a>suffix</p>
</td>
<td class="cellrowborder" valign="top" width="18.93%" headers="mcps1.2.5.1.2 "><p id="p16510185319507"><a name="p16510185319507"></a><a name="p16510185319507"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59079892"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59079892"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59079892"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="44.3%" headers="mcps1.2.5.1.4 "><p id="p2502122213217"><a name="p2502122213217"></a><a name="p2502122213217"></a>批量托管时的文件后缀名列表。不传或传空值时，表示托管所有音视频文件，不进行后缀名过滤。</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row55081455"><td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p224314412295"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p224314412295"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p224314412295"></a>template_group_name</p>
</td>
<td class="cellrowborder" valign="top" width="18.93%" headers="mcps1.2.5.1.2 "><p id="p1366721410511"><a name="p1366721410511"></a><a name="p1366721410511"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p5244194112915"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p5244194112915"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p5244194112915"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.3%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p282452216325"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p282452216325"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p282452216325"></a>转码模板组名称。</p>
<p id="p2839171410302"><a name="p2839171410302"></a><a name="p2839171410302"></a>若不为空，则使用指定的转码模板对上传的音视频进行转码，您可以在视频点播控制台配置转码模板，具体请参见<a href="https://support.huaweicloud.com/usermanual-vod/vod_01_0072.html" target="_blank" rel="noopener noreferrer">转码设置</a>。</p>
<div class="note" id="note1110033814382"><a name="note1110033814382"></a><a name="note1110033814382"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1610033819389"><a name="p1610033819389"></a><a name="p1610033819389"></a>若同时设置了<span class="parmname" id="parmname178471651153819"><a name="parmname178471651153819"></a><a name="parmname178471651153819"></a>“template_group_name”</span>和<span class="parmname" id="parmname1089414103915"><a name="parmname1089414103915"></a><a name="parmname1089414103915"></a>“workflow_name”</span>字段，则<span class="parmname" id="parmname5281229397"><a name="parmname5281229397"></a><a name="parmname5281229397"></a>“template_group_name”</span>字段生效。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row49119006"><td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.5.1.1 "><p id="p14827123115351"><a name="p14827123115351"></a><a name="p14827123115351"></a>workflow_name</p>
</td>
<td class="cellrowborder" valign="top" width="18.93%" headers="mcps1.2.5.1.2 "><p id="p206721414195116"><a name="p206721414195116"></a><a name="p206721414195116"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.5.1.3 "><p id="p13709142911351"><a name="p13709142911351"></a><a name="p13709142911351"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.3%" headers="mcps1.2.5.1.4 "><p id="p877510281322"><a name="p877510281322"></a><a name="p877510281322"></a>工作流名称。</p>
<p id="p3873113319310"><a name="p3873113319310"></a><a name="p3873113319310"></a>若不为空，则使用指定的工作流对上传的音视频进行处理，您可以在视频点播控制台配置工作流，具体请参见<a href="https://support.huaweicloud.com/usermanual-vod/vod010041.html" target="_blank" rel="noopener noreferrer">工作流设置</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row2145301"><td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.5.1.1 "><p id="p12909143510350"><a name="p12909143510350"></a><a name="p12909143510350"></a>host_type</p>
</td>
<td class="cellrowborder" valign="top" width="18.93%" headers="mcps1.2.5.1.2 "><p id="p176778144511"><a name="p176778144511"></a><a name="p176778144511"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49572116"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49572116"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49572116"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="44.3%" headers="mcps1.2.5.1.4 "><p id="p651396142010"><a name="p651396142010"></a><a name="p651396142010"></a>表示音视频处理后生成的媒资文件所存储的位置类型。</p>
<div class="p" id="p19548207142019"><a name="p19548207142019"></a><a name="p19548207142019"></a>取值如下所示：<a name="ul3705153772010"></a><a name="ul3705153772010"></a><ul id="ul3705153772010"><li>0：表示存储到点播桶。</li><li>1：表示存储在租户桶。</li><li>2：表示存储到租户桶，并且存储路径与源文件一致。</li></ul>
</div>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row47843365"><td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.5.1.1 "><p id="p1375774443513"><a name="p1375774443513"></a><a name="p1375774443513"></a>output_bucket</p>
</td>
<td class="cellrowborder" valign="top" width="18.93%" headers="mcps1.2.5.1.2 "><p id="p166842142519"><a name="p166842142519"></a><a name="p166842142519"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32161874"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32161874"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32161874"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.3%" headers="mcps1.2.5.1.4 "><p id="p78541330203420"><a name="p78541330203420"></a><a name="p78541330203420"></a>输出桶名，host_type为1时必选</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row18718889915"><td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.5.1.1 "><p id="p14346134803518"><a name="p14346134803518"></a><a name="p14346134803518"></a>output_path</p>
</td>
<td class="cellrowborder" valign="top" width="18.93%" headers="mcps1.2.5.1.2 "><p id="p106893145515"><a name="p106893145515"></a><a name="p106893145515"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.5.1.3 "><p id="p1206984582"><a name="p1206984582"></a><a name="p1206984582"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.3%" headers="mcps1.2.5.1.4 "><p id="p1876611289324"><a name="p1876611289324"></a><a name="p1876611289324"></a>输出路径名，host_type为1时必选</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section126831744152813"></a>

```
{
   "bucket": "obs-gg",
   "object": "1/Shoushu_FLV.flv",
   "suffix": [],
   "template_group_name": "original_template_group",
   "host_type" : 1,
   "output_bucket" : "obs-gg",
   "output_path" : "ouput/"
}
```

## 返回参数<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section1758182152916"></a>

-   **处理成功时返回**

    **表 4**  处理成功返回参数

    <a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_table162710272419"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_row99616271442"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p149611527042"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p149611527042"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p149611527042"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1962627444"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1962627444"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1962627444"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p3961192717419"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p3961192717419"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p3961192717419"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_row1496252717415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p9963727344"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p9963727344"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p9963727344"></a>task_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1596382713413"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1596382713413"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1596382713413"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p04681454474"><a name="p04681454474"></a><a name="p04681454474"></a>任务ID。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   **处理失败时返回**

    **表 5**  处理失败返回参数

    <a name="table7878165410215"></a>
    <table><thead align="left"><tr id="row12878125415218"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p108791754182117"><a name="p108791754182117"></a><a name="p108791754182117"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1687955418219"><a name="p1687955418219"></a><a name="p1687955418219"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p20879155422114"><a name="p20879155422114"></a><a name="p20879155422114"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row11879165413212"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1487917543217"><a name="p1487917543217"></a><a name="p1487917543217"></a>error_code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1087916543211"><a name="p1087916543211"></a><a name="p1087916543211"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p28791054112115"><a name="p28791054112115"></a><a name="p28791054112115"></a>错误码。</p>
    </td>
    </tr>
    <tr id="row2879105492118"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1087925402119"><a name="p1087925402119"></a><a name="p1087925402119"></a>error_msg</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1487916547216"><a name="p1487916547216"></a><a name="p1487916547216"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p18794548213"><a name="p18794548213"></a><a name="p18794548213"></a>错误描述。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 返回示例<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section175034214305"></a>

-   处理成功返回（200 OK）

    ```
    {
      "task_id": "456"
    }
    ```

-   处理失败返回（400 Bad Request）

    ```
    {
      "error_code": "VOD.10053",
      "error_msg": "请求参数非法，非法字段：status"
    }
    ```


## 错误码<a name="section569214377267"></a>

错误码请参见[错误码](错误码.md)。

