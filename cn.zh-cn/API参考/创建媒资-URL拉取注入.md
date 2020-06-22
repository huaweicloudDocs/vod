# 创建媒资：URL拉取注入<a name="vod_04_0052"></a>

## 功能介绍<a name="section4915145617137"></a>

基于音视频源文件URL，将音视频文件离线拉取上传到点播服务。

## 调试<a name="section8345114810114"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=VOD&api=uploadMetaDataByUrl)中直接运行调试该接口。

## URI<a name="section1267575319524"></a>

POST /v1.0/\{[project\_id](获取项目ID.md)\}/asset/upload\_by\_url

## 请求参数<a name="section1933373275414"></a>

**表 1**  请求参数

<a name="table74725217556"></a>
<table><thead align="left"><tr id="row747310205515"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p64743265511"><a name="p64743265511"></a><a name="p64743265511"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p1947422165516"><a name="p1947422165516"></a><a name="p1947422165516"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="p5474326551"><a name="p5474326551"></a><a name="p5474326551"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="p20474626557"><a name="p20474626557"></a><a name="p20474626557"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="row947419205511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p992219262575"><a name="p992219262575"></a><a name="p992219262575"></a>upload_metadatas</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p4474172175517"><a name="p4474172175517"></a><a name="p4474172175517"></a>Array of <a href="#table114403491596">upload_metadata</a> objects</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p84741522554"><a name="p84741522554"></a><a name="p84741522554"></a>待拉取创建的媒资元数据列表。一次最多支持16个。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p547542185513"><a name="p547542185513"></a><a name="p547542185513"></a>M</p>
</td>
</tr>
</tbody>
</table>

**表 2**  upload\_metadata参数说明

<a name="table114403491596"></a>
<table><thead align="left"><tr id="row944164985910"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p17441749135919"><a name="p17441749135919"></a><a name="p17441749135919"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p244234920596"><a name="p244234920596"></a><a name="p244234920596"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="p1044314945911"><a name="p1044314945911"></a><a name="p1044314945911"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="p194431749175911"><a name="p194431749175911"></a><a name="p194431749175911"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="row164432495593"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1244364955915"><a name="p1244364955915"></a><a name="p1244364955915"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p17443104945920"><a name="p17443104945920"></a><a name="p17443104945920"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p1344312491599"><a name="p1344312491599"></a><a name="p1344312491599"></a>视频源文件URL。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p844317499596"><a name="p844317499596"></a><a name="p844317499596"></a>M</p>
</td>
</tr>
<tr id="row244311492598"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p74431149175912"><a name="p74431149175912"></a><a name="p74431149175912"></a>title</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p24441349165913"><a name="p24441349165913"></a><a name="p24441349165913"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p0444194914593"><a name="p0444194914593"></a><a name="p0444194914593"></a>媒资标题，长度不超过128个字节，UTF-8编码。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p1444411493593"><a name="p1444411493593"></a><a name="p1444411493593"></a>M</p>
</td>
</tr>
<tr id="row14444184945918"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p18445144918591"><a name="p18445144918591"></a><a name="p18445144918591"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p544518495592"><a name="p544518495592"></a><a name="p544518495592"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p744604985917"><a name="p744604985917"></a><a name="p744604985917"></a>视频描述，长度不超过1024个字节。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p9446154985916"><a name="p9446154985916"></a><a name="p9446154985916"></a>O</p>
</td>
</tr>
<tr id="row7446749165920"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p19446549125920"><a name="p19446549125920"></a><a name="p19446549125920"></a>category_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p8446154916596"><a name="p8446154916596"></a><a name="p8446154916596"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p49483440"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p49483440"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p49483440"></a>媒资分类ID。</p>
<p id="p1113582020331"><a name="p1113582020331"></a><a name="p1113582020331"></a>若不为空，则可以将上传的音视频归类到指定分类中，您可以在视频点播控制台配置分类，具体请参见<a href="https://support.huaweicloud.com/usermanual-vod/vod010006.html" target="_blank" rel="noopener noreferrer">分类设置</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p644712496592"><a name="p644712496592"></a><a name="p644712496592"></a>O</p>
</td>
</tr>
<tr id="row14474496591"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p0447154914599"><a name="p0447154914599"></a><a name="p0447154914599"></a>video_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p844724995919"><a name="p844724995919"></a><a name="p844724995919"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p55918423"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p55918423"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p55918423"></a>拉取的音视频文件类型。</p>
<div class="p" id="p1042719724118"><a name="p1042719724118"></a><a name="p1042719724118"></a>取值如下：<a name="ul0436102264110"></a><a name="ul0436102264110"></a><ul id="ul0436102264110"><li>视频文件：MP4、TS、MOV、MXF、MPG、FLV、WMV、AVI、M4V、F4V、MPEG、3GP、ASF、MKV</li><li>音频文件：MP3、OGG、WAV、WMA、APE、FLAC、AAC、AC3、MMF、AMR、M4A、M4R、WV、MP2</li></ul>
</div>
<p id="p151452038191311"><a name="p151452038191311"></a><a name="p151452038191311"></a>若上传格式为音频文件，则不支持转码、添加水印和字幕。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p54471849155918"><a name="p54471849155918"></a><a name="p54471849155918"></a>M</p>
</td>
</tr>
<tr id="row844724911592"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1244714915913"><a name="p1244714915913"></a><a name="p1244714915913"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p16447749135914"><a name="p16447749135914"></a><a name="p16447749135914"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p175919618333"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p175919618333"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p175919618333"></a>视频标签。</p>
<p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177381053319"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177381053319"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p177381053319"></a>单个标签不超过16个字节，最多不超过16个标签。</p>
<p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p54975040"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p54975040"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p54975040"></a>多个用逗号分隔，UTF8编码。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p3448149105918"><a name="p3448149105918"></a><a name="p3448149105918"></a>O</p>
</td>
</tr>
<tr id="row1644874975912"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1944894918596"><a name="p1944894918596"></a><a name="p1944894918596"></a>auto_publish</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p5448114913591"><a name="p5448114913591"></a><a name="p5448114913591"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p12216105010336"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p12216105010336"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p12216105010336"></a>是否自动发布。</p>
<div class="p" id="p132071938184119"><a name="p132071938184119"></a><a name="p132071938184119"></a>取值如下：<a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_ul0549132123415"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_ul0549132123415"></a><ul id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_ul0549132123415"><li>0：表示不自动发布。</li><li>1：表示自动发布。</li></ul>
</div>
<p id="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p288132373411"><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p288132373411"></a><a name="zh-cn_topic_0128109922_zh-cn_topic_0127940850_p288132373411"></a>默认值：1。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p17448349155918"><a name="p17448349155918"></a><a name="p17448349155918"></a>O</p>
</td>
</tr>
<tr id="row184801791009"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p224314412295"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p224314412295"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p224314412295"></a>template_group_name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p5244194112915"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p5244194112915"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p5244194112915"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p282452216325"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p282452216325"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p282452216325"></a>转码模板组名称。</p>
<p id="p2839171410302"><a name="p2839171410302"></a><a name="p2839171410302"></a>若不为空，则使用指定的转码模板对上传的音视频进行转码，您可以在视频点播控制台配置转码模板，具体请参见<a href="https://support.huaweicloud.com/usermanual-vod/vod_01_0072.html" target="_blank" rel="noopener noreferrer">转码设置</a>。</p>
<div class="note" id="note1110033814382"><a name="note1110033814382"></a><a name="note1110033814382"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1610033819389"><a name="p1610033819389"></a><a name="p1610033819389"></a>若同时设置了<span class="parmname" id="parmname178471651153819"><a name="parmname178471651153819"></a><a name="parmname178471651153819"></a>“template_group_name”</span>和<span class="parmname" id="parmname1089414103915"><a name="parmname1089414103915"></a><a name="parmname1089414103915"></a>“workflow_name”</span>字段，则<span class="parmname" id="parmname5281229397"><a name="parmname5281229397"></a><a name="parmname5281229397"></a>“template_group_name”</span>字段生效。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p1324417418295"><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p1324417418295"></a><a name="zh-cn_topic_0128109898_zh-cn_topic_0127940846_p1324417418295"></a>O</p>
</td>
</tr>
<tr id="row4739172493714"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p14827123115351"><a name="p14827123115351"></a><a name="p14827123115351"></a>workflow_name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p13709142911351"><a name="p13709142911351"></a><a name="p13709142911351"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p877510281322"><a name="p877510281322"></a><a name="p877510281322"></a>工作流名称。</p>
<p id="p3873113319310"><a name="p3873113319310"></a><a name="p3873113319310"></a>若不为空，则使用指定的工作流对上传的音视频进行处理，您可以在视频点播控制台配置工作流，具体请参见<a href="https://support.huaweicloud.com/usermanual-vod/vod010041.html" target="_blank" rel="noopener noreferrer">工作流设置</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p870922953518"><a name="p870922953518"></a><a name="p870922953518"></a>O</p>
</td>
</tr>
<tr id="row924318148018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p202441141704"><a name="p202441141704"></a><a name="p202441141704"></a>auto_encrypt</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p42441141106"><a name="p42441141106"></a><a name="p42441141106"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p17572187432"><a name="p17572187432"></a><a name="p17572187432"></a>是否自动加密。</p>
<div class="p" id="p1471445844110"><a name="p1471445844110"></a><a name="p1471445844110"></a>取值如下：<a name="ul1019513284317"></a><a name="ul1019513284317"></a><ul id="ul1019513284317"><li>0：表示不加密。</li><li>1：表示需要加密。</li></ul>
</div>
<p id="p516644804317"><a name="p516644804317"></a><a name="p516644804317"></a>默认值：0。</p>
<p id="p427823717424"><a name="p427823717424"></a><a name="p427823717424"></a>若设置为需要加密，则必须配置转码模板，且转码的输出格式是HLS。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p202441414506"><a name="p202441414506"></a><a name="p202441414506"></a>O</p>
</td>
</tr>
<tr id="row1813719188011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p813710184013"><a name="p813710184013"></a><a name="p813710184013"></a>thumbnail</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p01371918803"><a name="p01371918803"></a><a name="p01371918803"></a><a href="#table22291146121512">Thumbnail</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p144391731290"><a name="p144391731290"></a><a name="p144391731290"></a>截图参数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p913818181209"><a name="p913818181209"></a><a name="p913818181209"></a>O</p>
</td>
</tr>
<tr id="row173369213018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p183375211108"><a name="p183375211108"></a><a name="p183375211108"></a>review</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p10337142112016"><a name="p10337142112016"></a><a name="p10337142112016"></a><a href="#table139381435171712">Review</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="p1139210371192"><a name="p1139210371192"></a><a name="p1139210371192"></a>审核参数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="p533719211400"><a name="p533719211400"></a><a name="p533719211400"></a>O</p>
</td>
</tr>
</tbody>
</table>

**表 3**  Thumbnail参数说明

<a name="table22291146121512"></a>
<table><thead align="left"><tr id="vod_04_0196_row6236110565"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="vod_04_0196_p1523610566"><a name="vod_04_0196_p1523610566"></a><a name="vod_04_0196_p1523610566"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="vod_04_0196_p62361501866"><a name="vod_04_0196_p62361501866"></a><a name="vod_04_0196_p62361501866"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="vod_04_0196_p17236100763"><a name="vod_04_0196_p17236100763"></a><a name="vod_04_0196_p17236100763"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="vod_04_0196_p142361406618"><a name="vod_04_0196_p142361406618"></a><a name="vod_04_0196_p142361406618"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="vod_04_0196_row423610366"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p123610966"><a name="vod_04_0196_p123610966"></a><a name="vod_04_0196_p123610966"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p15236150161"><a name="vod_04_0196_p15236150161"></a><a name="vod_04_0196_p15236150161"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p102361502062"><a name="vod_04_0196_p102361502062"></a><a name="vod_04_0196_p102361502062"></a>截图类型。</p>
<p id="vod_04_0196_p1832519442142"><a name="vod_04_0196_p1832519442142"></a><a name="vod_04_0196_p1832519442142"></a>取值如下：</p>
<a name="vod_04_0196_ul6492111332810"></a><a name="vod_04_0196_ul6492111332810"></a><ul id="vod_04_0196_ul6492111332810"><li>time：每次进行截图的间隔时间。</li><li>dots : 按照指定的时间点截图。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p162361300611"><a name="vod_04_0196_p162361300611"></a><a name="vod_04_0196_p162361300611"></a>M</p>
</td>
</tr>
<tr id="vod_04_0196_row223650264"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p1023612013619"><a name="vod_04_0196_p1023612013619"></a><a name="vod_04_0196_p1023612013619"></a>time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p123620669"><a name="vod_04_0196_p123620669"></a><a name="vod_04_0196_p123620669"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p19236600620"><a name="vod_04_0196_p19236600620"></a><a name="vod_04_0196_p19236600620"></a>生成截图的时间间隔值。</p>
<p id="vod_04_0196_p19116144333617"><a name="vod_04_0196_p19116144333617"></a><a name="vod_04_0196_p19116144333617"></a>取值范围：[1,12]之间的整数。</p>
<p id="vod_04_0196_p135114883713"><a name="vod_04_0196_p135114883713"></a><a name="vod_04_0196_p135114883713"></a>单位：秒。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p52365012614"><a name="vod_04_0196_p52365012614"></a><a name="vod_04_0196_p52365012614"></a>O</p>
</td>
</tr>
<tr id="vod_04_0196_row4236130163"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p1923617018618"><a name="vod_04_0196_p1923617018618"></a><a name="vod_04_0196_p1923617018618"></a>dots</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p42361603616"><a name="vod_04_0196_p42361603616"></a><a name="vod_04_0196_p42361603616"></a>Array of integers</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p823619015619"><a name="vod_04_0196_p823619015619"></a><a name="vod_04_0196_p823619015619"></a>指定时间截图时的时间点数组。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p112361101167"><a name="vod_04_0196_p112361101167"></a><a name="vod_04_0196_p112361101167"></a>O</p>
</td>
</tr>
<tr id="vod_04_0196_row82368013616"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p42361019619"><a name="vod_04_0196_p42361019619"></a><a name="vod_04_0196_p42361019619"></a>cover_position</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p4236501968"><a name="vod_04_0196_p4236501968"></a><a name="vod_04_0196_p4236501968"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p127841362196"><a name="vod_04_0196_p127841362196"></a><a name="vod_04_0196_p127841362196"></a>指定第几张截图作为封面。</p>
<p id="vod_04_0196_p72361603610"><a name="vod_04_0196_p72361603610"></a><a name="vod_04_0196_p72361603610"></a>默认值：1。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p132362004611"><a name="vod_04_0196_p132362004611"></a><a name="vod_04_0196_p132362004611"></a>O</p>
</td>
</tr>
<tr id="vod_04_0196_row18236190165"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p192361302069"><a name="vod_04_0196_p192361302069"></a><a name="vod_04_0196_p192361302069"></a>format</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p152361005619"><a name="vod_04_0196_p152361005619"></a><a name="vod_04_0196_p152361005619"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p2138182311812"><a name="vod_04_0196_p2138182311812"></a><a name="vod_04_0196_p2138182311812"></a>截图文件格式。</p>
<p id="vod_04_0196_p91092284183"><a name="vod_04_0196_p91092284183"></a><a name="vod_04_0196_p91092284183"></a>取值如下：</p>
<p id="vod_04_0196_p585515283820"><a name="vod_04_0196_p585515283820"></a><a name="vod_04_0196_p585515283820"></a>1：jpg。</p>
<p id="vod_04_0196_p171262495303"><a name="vod_04_0196_p171262495303"></a><a name="vod_04_0196_p171262495303"></a>默认值：1 。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p15236706613"><a name="vod_04_0196_p15236706613"></a><a name="vod_04_0196_p15236706613"></a>O</p>
</td>
</tr>
<tr id="vod_04_0196_row18236180368"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p102361001265"><a name="vod_04_0196_p102361001265"></a><a name="vod_04_0196_p102361001265"></a>aspect_ratio</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p102361301565"><a name="vod_04_0196_p102361301565"></a><a name="vod_04_0196_p102361301565"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p1921951017206"><a name="vod_04_0196_p1921951017206"></a><a name="vod_04_0196_p1921951017206"></a>纵横比，图像缩放方式。</p>
<div class="p" id="vod_04_0196_p44711160201"><a name="vod_04_0196_p44711160201"></a><a name="vod_04_0196_p44711160201"></a>取值如下：<a name="vod_04_0196_ul1346182262015"></a><a name="vod_04_0196_ul1346182262015"></a><ul id="vod_04_0196_ul1346182262015"><li>0：自适应（保持原有宽高比）。</li><li>1：16:9。</li></ul>
</div>
<p id="vod_04_0196_p162361701364"><a name="vod_04_0196_p162361701364"></a><a name="vod_04_0196_p162361701364"></a>默认值：0。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p162369013614"><a name="vod_04_0196_p162369013614"></a><a name="vod_04_0196_p162369013614"></a>O</p>
</td>
</tr>
<tr id="vod_04_0196_row13236100968"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p192361401063"><a name="vod_04_0196_p192361401063"></a><a name="vod_04_0196_p192361401063"></a>max_length</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p7236601562"><a name="vod_04_0196_p7236601562"></a><a name="vod_04_0196_p7236601562"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p11940248211"><a name="vod_04_0196_p11940248211"></a><a name="vod_04_0196_p11940248211"></a>截图最长边的尺寸。</p>
<p id="vod_04_0196_p88853118211"><a name="vod_04_0196_p88853118211"></a><a name="vod_04_0196_p88853118211"></a>单位：像素。</p>
<p id="vod_04_0196_p42361601162"><a name="vod_04_0196_p42361601162"></a><a name="vod_04_0196_p42361601162"></a>宽边尺寸按照该尺寸与原始视频像素等比缩放计算。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p92361202067"><a name="vod_04_0196_p92361202067"></a><a name="vod_04_0196_p92361202067"></a>O</p>
</td>
</tr>
</tbody>
</table>

**表 4**  Review参数说明

<a name="table139381435171712"></a>
<table><thead align="left"><tr id="vod_04_0196_row124991151087"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="vod_04_0196_p449905788"><a name="vod_04_0196_p449905788"></a><a name="vod_04_0196_p449905788"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="vod_04_0196_p164992053815"><a name="vod_04_0196_p164992053815"></a><a name="vod_04_0196_p164992053815"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.3"><p id="vod_04_0196_p104992512816"><a name="vod_04_0196_p104992512816"></a><a name="vod_04_0196_p104992512816"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.4"><p id="vod_04_0196_p1352110103520"><a name="vod_04_0196_p1352110103520"></a><a name="vod_04_0196_p1352110103520"></a>必选项（M）/可选项（O）</p>
</th>
</tr>
</thead>
<tbody><tr id="vod_04_0196_row5846612121812"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="vod_04_0196_p6846141218184"><a name="vod_04_0196_p6846141218184"></a><a name="vod_04_0196_p6846141218184"></a>template_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="vod_04_0196_p16846112181812"><a name="vod_04_0196_p16846112181812"></a><a name="vod_04_0196_p16846112181812"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.3 "><p id="vod_04_0196_p116163113286"><a name="vod_04_0196_p116163113286"></a><a name="vod_04_0196_p116163113286"></a>审核模板ID。</p>
<p id="vod_04_0196_p484616121185"><a name="vod_04_0196_p484616121185"></a><a name="vod_04_0196_p484616121185"></a>若不为空，则使用指定的模板ID对上传的音视频进行审核，您可以在视频点播控制台配置审核模板，具体请参见<a href="https://support.huaweicloud.com/usermanual-vod/vod_01_0057.html" target="_blank" rel="noopener noreferrer">审核设置</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.4 "><p id="vod_04_0196_p15846512101816"><a name="vod_04_0196_p15846512101816"></a><a name="vod_04_0196_p15846512101816"></a>M</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section16393758885"></a>

```
{
	"upload_metadatas":[
		{
			 "url": "https://mpc-test.obs.myhwclouds.com/Avatar_480P.mp4",	
			 "title": "Avatar test test",     
			 "video_type": "MP4",	
			 "description": "Avatar, test",
			 "category_id": 1,	
			 "tags":"mytags",	
			 "auto_publish": 1
		},
		{
			 "url": "https://mpc-test.obs.myhwclouds.com/Avatar_720.mp4",	
			 "title": "Avatar test test",     
			 "video_type": "MP4",	
			 "description": "Avatar, test",
			 "category_id": 1,	
			 "tags":"mytags",	
			 "auto_publish": 1
		}
		]

}
```

## 返回参数<a name="section1288123282713"></a>

-   **处理成功时返回**

    **表 5**  处理成功返回参数

    <a name="table20619133392911"></a>
    <table><thead align="left"><tr id="row06209338294"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p26201833112918"><a name="p26201833112918"></a><a name="p26201833112918"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p196211233142914"><a name="p196211233142914"></a><a name="p196211233142914"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p16620033132919"><a name="p16620033132919"></a><a name="p16620033132919"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row11621733162912"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p136222033202919"><a name="p136222033202919"></a><a name="p136222033202919"></a>upload_assets</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p3622233102916"><a name="p3622233102916"></a><a name="p3622233102916"></a>Array of <a href="#table1422513366329">UploadAsset</a> objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1162243342918"><a name="p1162243342918"></a><a name="p1162243342918"></a>新创建的媒资列表。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 6**  UploadAsset参数说明

    <a name="table1422513366329"></a>
    <table><thead align="left"><tr id="row18226183617321"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p112265368323"><a name="p112265368323"></a><a name="p112265368323"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1422612366325"><a name="p1422612366325"></a><a name="p1422612366325"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p15226123618323"><a name="p15226123618323"></a><a name="p15226123618323"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1022616367326"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1722613673217"><a name="p1722613673217"></a><a name="p1722613673217"></a>url</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p422614364328"><a name="p422614364328"></a><a name="p422614364328"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p19227143623218"><a name="p19227143623218"></a><a name="p19227143623218"></a>媒资所在URL。</p>
    </td>
    </tr>
    <tr id="row322793612323"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p2227133623214"><a name="p2227133623214"></a><a name="p2227133623214"></a>asset_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1922719364321"><a name="p1922719364321"></a><a name="p1922719364321"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1822711361326"><a name="p1822711361326"></a><a name="p1822711361326"></a>新创建媒资的媒资id。</p>
    </td>
    </tr>
    <tr id="row32271436113211"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1222819366328"><a name="p1222819366328"></a><a name="p1222819366328"></a>error_code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1422843683217"><a name="p1422843683217"></a><a name="p1422843683217"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p22281636173217"><a name="p22281636173217"></a><a name="p22281636173217"></a>错误码。</p>
    </td>
    </tr>
    <tr id="row81691931173312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p121691631203312"><a name="p121691631203312"></a><a name="p121691631203312"></a>error_msg</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p617011316331"><a name="p617011316331"></a><a name="p617011316331"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p617023120334"><a name="p617023120334"></a><a name="p617023120334"></a>错误描述。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   **处理失败时返回**

    **表 7**  处理失败返回参数

    <a name="table1533161014315"></a>
    <table><thead align="left"><tr id="row13325101316"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1733271010319"><a name="p1733271010319"></a><a name="p1733271010319"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p12332131093112"><a name="p12332131093112"></a><a name="p12332131093112"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p433217106310"><a name="p433217106310"></a><a name="p433217106310"></a>类型</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2332181010310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p13321610193113"><a name="p13321610193113"></a><a name="p13321610193113"></a>error_code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p3332181073114"><a name="p3332181073114"></a><a name="p3332181073114"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p833211053118"><a name="p833211053118"></a><a name="p833211053118"></a>错误码。</p>
    </td>
    </tr>
    <tr id="row63321510113119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p033216102318"><a name="p033216102318"></a><a name="p033216102318"></a>error_msg</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p7333210173114"><a name="p7333210173114"></a><a name="p7333210173114"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p4333141010317"><a name="p4333141010317"></a><a name="p4333141010317"></a>错误描述。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 返回示例<a name="section1394555193012"></a>

-   处理成功返回（200 OK）

    ```
    {
      "upload_assets": [
        {
          "url": "https://mpc-test.obs.myhwclouds.com/Avatar_480P.mp4",
          "asset_id": "f488337c31c8e4622f1590735b134c65",
          "error_code": null,
          "error_msg": null
        },
        {
          "url": "https://mpc-test.obs.myhwclouds.com/Avatar_720.mp4",
          "asset_id": "f488337c31c8e4622f1590525b134c65",
          "error_code": null,
          "error_msg": null
        },
    
      ]
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

