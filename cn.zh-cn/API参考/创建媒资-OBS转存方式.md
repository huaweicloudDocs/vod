# 创建媒资：OBS转存方式<a name="zh-cn_topic_0129004455"></a>

## 功能描述<a name="section157020365410"></a>

若您在使用点播服务前，已经在OBS桶中存储了音视频文件，您可以使用该接口将存储在OBS桶中的音视频文件转存到点播服务中，使用点播服务的音视频管理功能。不同区域的云服务不能互连，所以待转存的OBS桶和点播服务必须在同一区域，如“华北-北京四”OBS桶中的音视频只能转存到“华北-北京四”点播服务中。

![](figures/OBS转存流程图新.png)

## 请求URI<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section5627230172812"></a>

POST /v1.0/\{[project\_id](获取项目ID.md)\}/asset/reproduction

## 请求参数<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section13573338112812"></a>

**表 1**  请求参数

<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_table11962631"></a>
<table><thead align="left"><tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row4709306"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p45909486"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p45909486"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p45909486"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27680879"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27680879"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27680879"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27558692"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27558692"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27558692"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="p512895812224"><a name="p512895812224"></a><a name="p512895812224"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row14539135243618"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p35404528369"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p35404528369"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p35404528369"></a>input</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p18540105216368"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p18540105216368"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p18540105216368"></a><a href="#table12261237151119">file_addr</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p13540145253619"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p13540145253619"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p13540145253619"></a>待发布媒资地址。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p155408523369"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p155408523369"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p155408523369"></a>M</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row57482668"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p25584516"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p25584516"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p25584516"></a>title</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59079892"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59079892"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59079892"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p20741957"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p20741957"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p20741957"></a>媒资标题，长度不超过128个字节，UTF-8编码。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p58315944"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p58315944"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p58315944"></a>M</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row55081455"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32412869"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32412869"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32412869"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p8196703"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p8196703"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p8196703"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59953189"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59953189"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p59953189"></a>视频描述，长度不超过1024个字节。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27827288"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27827288"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p27827288"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row49119006"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p19216572"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p19216572"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p19216572"></a>category_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p13038474"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p13038474"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p13038474"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49483440"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49483440"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49483440"></a>媒资分类id。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p55277862"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p55277862"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p55277862"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row2145301"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p39551712"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p39551712"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p39551712"></a>video_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49572116"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49572116"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p49572116"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p55918423"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p55918423"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p55918423"></a>转存的音视频文件类型。</p>
<div class="p" id="p1042719724118"><a name="p1042719724118"></a><a name="p1042719724118"></a>取值如下：<a name="ul0436102264110"></a><a name="ul0436102264110"></a><ul id="ul0436102264110"><li>视频文件：MP4、TS、MOV、MXF、MPG、FLV、WMV、AVI、M4V、F4V、MPEG、3GP、ASF、MKV<p id="p311413012124"><a name="p311413012124"></a><a name="p311413012124"></a></p>
</li><li>音频文件：MP3、OGG、WAV、WMA、APE、FLAC、AAC、AC3、MMF、AMR、M4A、M4R、WV、MP2</li></ul>
</div>
<p id="p151452038191311"><a name="p151452038191311"></a><a name="p151452038191311"></a>若上传格式为音频文件，则不支持转码，添加水印，添加字幕。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p36689595"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p36689595"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p36689595"></a>M</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row47843365"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p50107329"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p50107329"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p50107329"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32161874"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32161874"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p32161874"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p175919618333"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p175919618333"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p175919618333"></a>视频标签。</p>
<p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177381053319"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177381053319"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177381053319"></a>单个标签不超过16个字节，最多不超过16个标签。</p>
<p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p54975040"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p54975040"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p54975040"></a>多个用逗号分隔，UTF8编码。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p48206417"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p48206417"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p48206417"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row18718889915"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p44542441"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p44542441"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p44542441"></a>auto_publish</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p51167958"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p51167958"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p51167958"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p12216105010336"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p12216105010336"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p12216105010336"></a>是否自动发布。</p>
<div class="p" id="p132071938184119"><a name="p132071938184119"></a><a name="p132071938184119"></a>取值如下：<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_ul0549132123415"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_ul0549132123415"></a><ul id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_ul0549132123415"><li>0：表示不自动发布。</li><li>1：表示自动发布。</li></ul>
</div>
<p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p288132373411"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p288132373411"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p288132373411"></a>默认值：1。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p37890287"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p37890287"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p37890287"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_row7768203416911"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177701234797"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177701234797"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177701234797"></a>template_group_name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p1177043416912"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p1177043416912"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p1177043416912"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p877011341799"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p877011341799"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p877011341799"></a>转码模板组名称。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p1977020345910"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p1977020345910"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p1977020345910"></a>O</p>
</td>
</tr>
<tr id="row1336123217263"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p636116327269"><a name="p636116327269"></a><a name="p636116327269"></a>auto_encrypt</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p9361832182618"><a name="p9361832182618"></a><a name="p9361832182618"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p17572187432"><a name="p17572187432"></a><a name="p17572187432"></a>是否自动加密。</p>
<div class="p" id="p1471445844110"><a name="p1471445844110"></a><a name="p1471445844110"></a>取值如下：<a name="ul1019513284317"></a><a name="ul1019513284317"></a><ul id="ul1019513284317"><li>0：表示不加密。</li><li>1：表示需要加密。</li></ul>
</div>
<p id="p516644804317"><a name="p516644804317"></a><a name="p516644804317"></a>默认值：0。</p>
<p id="p427823717424"><a name="p427823717424"></a><a name="p427823717424"></a>若设置为需要加密，则必须配置转码模板，且转码的输出格式是HLS。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p12375032182612"><a name="p12375032182612"></a><a name="p12375032182612"></a>O</p>
</td>
</tr>
<tr id="row184393311193"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p144397314917"><a name="p144397314917"></a><a name="p144397314917"></a>thumbnail</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p543913111910"><a name="p543913111910"></a><a name="p543913111910"></a><a href="#table22291146121512">Thumbnail</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p144391731290"><a name="p144391731290"></a><a name="p144391731290"></a>截图参数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p043914311293"><a name="p043914311293"></a><a name="p043914311293"></a>O</p>
</td>
</tr>
<tr id="row103921437898"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1439210371695"><a name="p1439210371695"></a><a name="p1439210371695"></a>review</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p33921371914"><a name="p33921371914"></a><a name="p33921371914"></a><a href="#table139381435171712">Review</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p1139210371192"><a name="p1139210371192"></a><a name="p1139210371192"></a>审核参数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p93927371791"><a name="p93927371791"></a><a name="p93927371791"></a>O</p>
</td>
</tr>
</tbody>
</table>

**表 2**  file\_addr参数说明

<a name="table12261237151119"></a>
<table><thead align="left"><tr id="row18226113720118"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p15226203731113"><a name="p15226203731113"></a><a name="p15226203731113"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p10227937111119"><a name="p10227937111119"></a><a name="p10227937111119"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="p172273370111"><a name="p172273370111"></a><a name="p172273370111"></a>参数描述</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="p1122718374118"><a name="p1122718374118"></a><a name="p1122718374118"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="row622714376112"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p7227937171110"><a name="p7227937171110"></a><a name="p7227937171110"></a>bucket</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p182276373114"><a name="p182276373114"></a><a name="p182276373114"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p19739142818429"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p19739142818429"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p19739142818429"></a>OBS的bucket名称。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p162271237181116"><a name="p162271237181116"></a><a name="p162271237181116"></a>M</p>
</td>
</tr>
<tr id="row1522713717119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1922719376119"><a name="p1922719376119"></a><a name="p1922719376119"></a>location</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p20228637121117"><a name="p20228637121117"></a><a name="p20228637121117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p97396282425"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p97396282425"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p97396282425"></a><span>桶所在的区域名， 如</span><span>“华北-北京四”</span><span>的区域名为</span><span>“cn-north-4”，创建的桶所在区域必须和点播服务所在区域保持一致。</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p122287374117"><a name="p122287374117"></a><a name="p122287374117"></a>M</p>
</td>
</tr>
<tr id="row11228163716114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p122286372115"><a name="p122286372115"></a><a name="p122286372115"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p19228183716117"><a name="p19228183716117"></a><a name="p19228183716117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p19177196164311"><a name="p19177196164311"></a><a name="p19177196164311"></a><span>文件的存储路径。</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p8228103710117"><a name="p8228103710117"></a><a name="p8228103710117"></a>M</p>
</td>
</tr>
</tbody>
</table>

**表 3**  Thumbnail参数说明

<a name="table22291146121512"></a>
<table><thead align="left"><tr id="zh-cn_topic_0129004451_row6236110565"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0129004451_p1523610566"><a name="zh-cn_topic_0129004451_p1523610566"></a><a name="zh-cn_topic_0129004451_p1523610566"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0129004451_p62361501866"><a name="zh-cn_topic_0129004451_p62361501866"></a><a name="zh-cn_topic_0129004451_p62361501866"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0129004451_p17236100763"><a name="zh-cn_topic_0129004451_p17236100763"></a><a name="zh-cn_topic_0129004451_p17236100763"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0129004451_p142361406618"><a name="zh-cn_topic_0129004451_p142361406618"></a><a name="zh-cn_topic_0129004451_p142361406618"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0129004451_row423610366"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p123610966"><a name="zh-cn_topic_0129004451_p123610966"></a><a name="zh-cn_topic_0129004451_p123610966"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p15236150161"><a name="zh-cn_topic_0129004451_p15236150161"></a><a name="zh-cn_topic_0129004451_p15236150161"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p102361502062"><a name="zh-cn_topic_0129004451_p102361502062"></a><a name="zh-cn_topic_0129004451_p102361502062"></a>截图类型。</p>
<p id="zh-cn_topic_0129004451_p1832519442142"><a name="zh-cn_topic_0129004451_p1832519442142"></a><a name="zh-cn_topic_0129004451_p1832519442142"></a>取值如下：</p>
<p id="zh-cn_topic_0129004451_p18201145463713"><a name="zh-cn_topic_0129004451_p18201145463713"></a><a name="zh-cn_topic_0129004451_p18201145463713"></a>time：每次进行截图的间隔时间。</p>
<p id="zh-cn_topic_0129004451_p1951613492173"><a name="zh-cn_topic_0129004451_p1951613492173"></a><a name="zh-cn_topic_0129004451_p1951613492173"></a>dots : 按照指定的时间点截图。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p162361300611"><a name="zh-cn_topic_0129004451_p162361300611"></a><a name="zh-cn_topic_0129004451_p162361300611"></a>M</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row223650264"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p1023612013619"><a name="zh-cn_topic_0129004451_p1023612013619"></a><a name="zh-cn_topic_0129004451_p1023612013619"></a>time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p123620669"><a name="zh-cn_topic_0129004451_p123620669"></a><a name="zh-cn_topic_0129004451_p123620669"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p19236600620"><a name="zh-cn_topic_0129004451_p19236600620"></a><a name="zh-cn_topic_0129004451_p19236600620"></a>生成截图的时间间隔值。</p>
<p id="zh-cn_topic_0129004451_p19116144333617"><a name="zh-cn_topic_0129004451_p19116144333617"></a><a name="zh-cn_topic_0129004451_p19116144333617"></a>取值范围：[1,12]之间的整数。</p>
<p id="zh-cn_topic_0129004451_p135114883713"><a name="zh-cn_topic_0129004451_p135114883713"></a><a name="zh-cn_topic_0129004451_p135114883713"></a>单位：秒</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p52365012614"><a name="zh-cn_topic_0129004451_p52365012614"></a><a name="zh-cn_topic_0129004451_p52365012614"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row4236130163"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p1923617018618"><a name="zh-cn_topic_0129004451_p1923617018618"></a><a name="zh-cn_topic_0129004451_p1923617018618"></a>dots</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p42361603616"><a name="zh-cn_topic_0129004451_p42361603616"></a><a name="zh-cn_topic_0129004451_p42361603616"></a>Array of integers</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p823619015619"><a name="zh-cn_topic_0129004451_p823619015619"></a><a name="zh-cn_topic_0129004451_p823619015619"></a>指定时间截图时的时间点数组。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p112361101167"><a name="zh-cn_topic_0129004451_p112361101167"></a><a name="zh-cn_topic_0129004451_p112361101167"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row82368013616"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p42361019619"><a name="zh-cn_topic_0129004451_p42361019619"></a><a name="zh-cn_topic_0129004451_p42361019619"></a>cover_position</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p4236501968"><a name="zh-cn_topic_0129004451_p4236501968"></a><a name="zh-cn_topic_0129004451_p4236501968"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p127841362196"><a name="zh-cn_topic_0129004451_p127841362196"></a><a name="zh-cn_topic_0129004451_p127841362196"></a>指定第几张截图作为封面。</p>
<p id="zh-cn_topic_0129004451_p72361603610"><a name="zh-cn_topic_0129004451_p72361603610"></a><a name="zh-cn_topic_0129004451_p72361603610"></a>默认值：1。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p132362004611"><a name="zh-cn_topic_0129004451_p132362004611"></a><a name="zh-cn_topic_0129004451_p132362004611"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row18236190165"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p192361302069"><a name="zh-cn_topic_0129004451_p192361302069"></a><a name="zh-cn_topic_0129004451_p192361302069"></a>format</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p152361005619"><a name="zh-cn_topic_0129004451_p152361005619"></a><a name="zh-cn_topic_0129004451_p152361005619"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p2138182311812"><a name="zh-cn_topic_0129004451_p2138182311812"></a><a name="zh-cn_topic_0129004451_p2138182311812"></a>截图文件格式。</p>
<p id="zh-cn_topic_0129004451_p91092284183"><a name="zh-cn_topic_0129004451_p91092284183"></a><a name="zh-cn_topic_0129004451_p91092284183"></a>取值如下：</p>
<p id="zh-cn_topic_0129004451_p585515283820"><a name="zh-cn_topic_0129004451_p585515283820"></a><a name="zh-cn_topic_0129004451_p585515283820"></a>1：jpg。</p>
<p id="zh-cn_topic_0129004451_p171262495303"><a name="zh-cn_topic_0129004451_p171262495303"></a><a name="zh-cn_topic_0129004451_p171262495303"></a>默认值：1 。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p15236706613"><a name="zh-cn_topic_0129004451_p15236706613"></a><a name="zh-cn_topic_0129004451_p15236706613"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row18236180368"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p102361001265"><a name="zh-cn_topic_0129004451_p102361001265"></a><a name="zh-cn_topic_0129004451_p102361001265"></a>aspect_ratio</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p102361301565"><a name="zh-cn_topic_0129004451_p102361301565"></a><a name="zh-cn_topic_0129004451_p102361301565"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p1921951017206"><a name="zh-cn_topic_0129004451_p1921951017206"></a><a name="zh-cn_topic_0129004451_p1921951017206"></a>纵横比，图像缩放方式。</p>
<div class="p" id="zh-cn_topic_0129004451_p44711160201"><a name="zh-cn_topic_0129004451_p44711160201"></a><a name="zh-cn_topic_0129004451_p44711160201"></a>取值如下：<a name="zh-cn_topic_0129004451_ul1346182262015"></a><a name="zh-cn_topic_0129004451_ul1346182262015"></a><ul id="zh-cn_topic_0129004451_ul1346182262015"><li>0：自适应（保持原有宽高比）。</li><li>1：16:9。</li></ul>
</div>
<p id="zh-cn_topic_0129004451_p162361701364"><a name="zh-cn_topic_0129004451_p162361701364"></a><a name="zh-cn_topic_0129004451_p162361701364"></a>默认值：0。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p162369013614"><a name="zh-cn_topic_0129004451_p162369013614"></a><a name="zh-cn_topic_0129004451_p162369013614"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row13236100968"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p192361401063"><a name="zh-cn_topic_0129004451_p192361401063"></a><a name="zh-cn_topic_0129004451_p192361401063"></a>max_length</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p7236601562"><a name="zh-cn_topic_0129004451_p7236601562"></a><a name="zh-cn_topic_0129004451_p7236601562"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p11940248211"><a name="zh-cn_topic_0129004451_p11940248211"></a><a name="zh-cn_topic_0129004451_p11940248211"></a>截图最长边的尺寸。</p>
<p id="zh-cn_topic_0129004451_p88853118211"><a name="zh-cn_topic_0129004451_p88853118211"></a><a name="zh-cn_topic_0129004451_p88853118211"></a>单位：像素。</p>
<p id="zh-cn_topic_0129004451_p42361601162"><a name="zh-cn_topic_0129004451_p42361601162"></a><a name="zh-cn_topic_0129004451_p42361601162"></a>宽边尺寸按照该尺寸与原始视频像素等比缩放计算。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p92361202067"><a name="zh-cn_topic_0129004451_p92361202067"></a><a name="zh-cn_topic_0129004451_p92361202067"></a>O</p>
</td>
</tr>
</tbody>
</table>

**表 4**  Review参数说明

<a name="table139381435171712"></a>
<table><thead align="left"><tr id="zh-cn_topic_0129004451_row124991151087"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0129004451_p449905788"><a name="zh-cn_topic_0129004451_p449905788"></a><a name="zh-cn_topic_0129004451_p449905788"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0129004451_p164992053815"><a name="zh-cn_topic_0129004451_p164992053815"></a><a name="zh-cn_topic_0129004451_p164992053815"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0129004451_p104992512816"><a name="zh-cn_topic_0129004451_p104992512816"></a><a name="zh-cn_topic_0129004451_p104992512816"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0129004451_p1352110103520"><a name="zh-cn_topic_0129004451_p1352110103520"></a><a name="zh-cn_topic_0129004451_p1352110103520"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0129004451_row16499135989"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p249919516814"><a name="zh-cn_topic_0129004451_p249919516814"></a><a name="zh-cn_topic_0129004451_p249919516814"></a>interval</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p1349915511816"><a name="zh-cn_topic_0129004451_p1349915511816"></a><a name="zh-cn_topic_0129004451_p1349915511816"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p94887566218"><a name="zh-cn_topic_0129004451_p94887566218"></a><a name="zh-cn_topic_0129004451_p94887566218"></a>截图的时间间隔。</p>
<p id="zh-cn_topic_0129004451_p55759372210"><a name="zh-cn_topic_0129004451_p55759372210"></a><a name="zh-cn_topic_0129004451_p55759372210"></a>取值范围：5或10。</p>
<p id="zh-cn_topic_0129004451_p13858102462216"><a name="zh-cn_topic_0129004451_p13858102462216"></a><a name="zh-cn_topic_0129004451_p13858102462216"></a>默认值：5</p>
<p id="zh-cn_topic_0129004451_p184521346194517"><a name="zh-cn_topic_0129004451_p184521346194517"></a><a name="zh-cn_topic_0129004451_p184521346194517"></a>单位：秒。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p134991750814"><a name="zh-cn_topic_0129004451_p134991750814"></a><a name="zh-cn_topic_0129004451_p134991750814"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row24992511819"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p1749917513814"><a name="zh-cn_topic_0129004451_p1749917513814"></a><a name="zh-cn_topic_0129004451_p1749917513814"></a>politics</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p8499352815"><a name="zh-cn_topic_0129004451_p8499352815"></a><a name="zh-cn_topic_0129004451_p8499352815"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p16205124216220"><a name="zh-cn_topic_0129004451_p16205124216220"></a><a name="zh-cn_topic_0129004451_p16205124216220"></a>进行政治人物检测时的置信度。</p>
<p id="zh-cn_topic_0129004451_p1749910512816"><a name="zh-cn_topic_0129004451_p1749910512816"></a><a name="zh-cn_topic_0129004451_p1749910512816"></a>取值范围：[-1,100]之间的整数。</p>
<div class="note" id="zh-cn_topic_0129004451_note1971311219236"><a name="zh-cn_topic_0129004451_note1971311219236"></a><a name="zh-cn_topic_0129004451_note1971311219236"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0129004451_ul1583016569291"></a><a name="zh-cn_topic_0129004451_ul1583016569291"></a><ul id="zh-cn_topic_0129004451_ul1583016569291"><li>未设置或设置为0时，表示不进行此项检测。</li><li>设置为-1 时，表示采用默认的置信度53。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p04999518810"><a name="zh-cn_topic_0129004451_p04999518810"></a><a name="zh-cn_topic_0129004451_p04999518810"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row14991851089"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p184991451817"><a name="zh-cn_topic_0129004451_p184991451817"></a><a name="zh-cn_topic_0129004451_p184991451817"></a>terrorism</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p949912518818"><a name="zh-cn_topic_0129004451_p949912518818"></a><a name="zh-cn_topic_0129004451_p949912518818"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p6438183042414"><a name="zh-cn_topic_0129004451_p6438183042414"></a><a name="zh-cn_topic_0129004451_p6438183042414"></a>进行暴恐元素检测时的置信度。</p>
<p id="zh-cn_topic_0129004451_p4513259818"><a name="zh-cn_topic_0129004451_p4513259818"></a><a name="zh-cn_topic_0129004451_p4513259818"></a>取值范围：为[-1,100]之间的整数。</p>
<div class="note" id="zh-cn_topic_0129004451_note16415194202413"><a name="zh-cn_topic_0129004451_note16415194202413"></a><a name="zh-cn_topic_0129004451_note16415194202413"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0129004451_ul173821755123012"></a><a name="zh-cn_topic_0129004451_ul173821755123012"></a><ul id="zh-cn_topic_0129004451_ul173821755123012"><li>未设置或设置为0时，表示不进行此项检测。</li><li>设置为-1 时， 表示采用默认的置信度80。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p1551314513811"><a name="zh-cn_topic_0129004451_p1551314513811"></a><a name="zh-cn_topic_0129004451_p1551314513811"></a>O</p>
</td>
</tr>
<tr id="zh-cn_topic_0129004451_row105131955815"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0129004451_p951317510811"><a name="zh-cn_topic_0129004451_p951317510811"></a><a name="zh-cn_topic_0129004451_p951317510811"></a>porn</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0129004451_p651345585"><a name="zh-cn_topic_0129004451_p651345585"></a><a name="zh-cn_topic_0129004451_p651345585"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0129004451_p19720165911246"><a name="zh-cn_topic_0129004451_p19720165911246"></a><a name="zh-cn_topic_0129004451_p19720165911246"></a>进行涉黄内容检测时的置信度。</p>
<p id="zh-cn_topic_0129004451_p551310515816"><a name="zh-cn_topic_0129004451_p551310515816"></a><a name="zh-cn_topic_0129004451_p551310515816"></a>取值范围：[-1,100]之间的整数。</p>
<div class="note" id="zh-cn_topic_0129004451_note92221912122512"><a name="zh-cn_topic_0129004451_note92221912122512"></a><a name="zh-cn_topic_0129004451_note92221912122512"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0129004451_ul123338192252"></a><a name="zh-cn_topic_0129004451_ul123338192252"></a><ul id="zh-cn_topic_0129004451_ul123338192252"><li>未设置或设置为0时，表示不进行此项检测。</li><li>设置为-1 时， 表示采用默认的置信度80。</li></ul>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0129004451_p95131853816"><a name="zh-cn_topic_0129004451_p95131853816"></a><a name="zh-cn_topic_0129004451_p95131853816"></a>O</p>
</td>
</tr>
</tbody>
</table>

## 请求样例<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section126831744152813"></a>

```
{
    "input": {
        "bucket": "bucket",
        "location": "cn-north-4",
        "object": "path"
    },
    "title": "title",
    "description": "des",
    "category_id": -1,
    "tags": "test",
    "video_type": "MP4",
    "auto_publish": 1,
    "template_group_name": "tempName"
}
```

## 返回参数<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section1758182152916"></a>

-   **处理成功时返回**

    **表 5**  处理成功返回参数

    <a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_table162710272419"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_row99616271442"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p149611527042"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p149611527042"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p149611527042"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1962627444"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1962627444"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1962627444"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p3961192717419"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p3961192717419"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p3961192717419"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_row1496252717415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p9963727344"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p9963727344"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p9963727344"></a>asset_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1596382713413"><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1596382713413"></a><a name="zh-cn_topic_0128109900_zh-cn_topic_0127940848_p1596382713413"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p04681454474"><a name="p04681454474"></a><a name="p04681454474"></a>媒资ID，UUID（通用唯一识别码）。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   **处理失败时返回**

    **表 6**  处理失败返回参数

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


## 返回样例<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_section175034214305"></a>

-   处理成功返回（200 OK）

    ```
    {
      "asset_id": "f488337c31c8e4622f1590735b134c65"
    }
    ```

-   处理失败返回（400 Bad Request）

    ```
    {
      "error_code": "VOD.10003",
      "error_msg": "The specified key does not exist."
    }
    ```


## 错误码<a name="section569214377267"></a>

错误码请参见[错误码](错误码.md)。

