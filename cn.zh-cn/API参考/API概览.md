# API概览<a name="vod_04_0001"></a>

视频点播服务对应的接口列表如下所示，在调用点播API前，您需要先获取用户Token，Token可以用于调用其他API时鉴权，具体如何调用点播API请参考[快速入门](媒资上传.md)。

## 媒资上传<a name="section1954516527125"></a>

<a name="table183487131317"></a>
<table><thead align="left"><tr id="row2311152631316"><th class="cellrowborder" valign="top" width="59.95%" id="mcps1.1.3.1.1"><p id="p731215260139"><a name="p731215260139"></a><a name="p731215260139"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="40.050000000000004%" id="mcps1.1.3.1.2"><p id="p4312112614139"><a name="p4312112614139"></a><a name="p4312112614139"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row168342711137"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p15835379133"><a name="p15835379133"></a><a name="p15835379133"></a>POST /v1.0/{project_id}/asset</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p20314131918149"><a name="p20314131918149"></a><a name="p20314131918149"></a><a href="创建媒资-上传方式.md">创建媒资：上传方式</a></p>
</td>
</tr>
<tr id="row198355741317"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p1883517717137"><a name="p1883517717137"></a><a name="p1883517717137"></a>GET /v1.1/{project_id}/asset/authority</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p33131519181411"><a name="p33131519181411"></a><a name="p33131519181411"></a><a href="获取分段上传授权.md">获取分段上传授权</a></p>
</td>
</tr>
<tr id="row78351679130"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p168357712138"><a name="p168357712138"></a><a name="p168357712138"></a>POST /v1.0/{project_id}/asset/status/uploaded</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1131221951412"><a name="p1131221951412"></a><a name="p1131221951412"></a><a href="确认媒资上传.md">确认媒资上传</a></p>
</td>
</tr>
<tr id="row88351570135"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p58351476134"><a name="p58351476134"></a><a name="p58351476134"></a>PUT /v1.0/{project_id}/asset/authority</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1031021910141"><a name="p1031021910141"></a><a name="p1031021910141"></a><a href="桶授权.md">桶授权</a></p>
</td>
</tr>
<tr id="row1583567161318"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p178356711139"><a name="p178356711139"></a><a name="p178356711139"></a>POST /v1.0/{project_id}/asset/reproduction</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p103098191147"><a name="p103098191147"></a><a name="p103098191147"></a><a href="创建媒资-OBS转存方式.md">创建媒资：OBS转存方式</a></p>
</td>
</tr>
<tr id="row85361041111519"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p1147944715155"><a name="p1147944715155"></a><a name="p1147944715155"></a>POST /v1.0/{project_id}/asset/reproduction</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p18536154115155"><a name="p18536154115155"></a><a name="p18536154115155"></a><a href="创建媒资-OBS托管方式.md">创建媒资：OBS托管方式</a></p>
</td>
</tr>
<tr id="row583557191319"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p1983516771311"><a name="p1983516771311"></a><a name="p1983516771311"></a>POST /v1.0/{project_id}/asset/upload_by_url</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1130811192144"><a name="p1130811192144"></a><a name="p1130811192144"></a><a href="创建媒资-URL拉取注入.md">创建媒资：URL拉取注入</a></p>
</td>
</tr>
<tr id="row88358716133"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p783517761312"><a name="p783517761312"></a><a name="p783517761312"></a>GET /v1.0/{project_id}/asset/duplication</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p030651911414"><a name="p030651911414"></a><a name="p030651911414"></a><a href="上传检验.md">上传检验</a></p>
</td>
</tr>
</tbody>
</table>

## 媒资预热<a name="section893685092412"></a>

<a name="table1966855842420"></a>
<table><thead align="left"><tr id="row1564713245257"><th class="cellrowborder" valign="top" width="59.95%" id="mcps1.1.3.1.1"><p id="p166477248253"><a name="p166477248253"></a><a name="p166477248253"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="40.050000000000004%" id="mcps1.1.3.1.2"><p id="p1764792412255"><a name="p1764792412255"></a><a name="p1764792412255"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row966825818243"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p866955882410"><a name="p866955882410"></a><a name="p866955882410"></a>POST /v1.0/{project_id}/asset/preheating</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p185497171851"><a name="p185497171851"></a><a name="p185497171851"></a><a href="媒资预热.md">媒资预热</a></p>
</td>
</tr>
<tr id="row3669185816241"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p18669115816241"><a name="p18669115816241"></a><a name="p18669115816241"></a>GET /v1.0/{project_id}/asset/preheating</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1766916581249"><a name="p1766916581249"></a><a name="p1766916581249"></a><a href="查询预热结果.md">查询预热结果</a></p>
</td>
</tr>
</tbody>
</table>

## 媒资管理<a name="section6123543193"></a>

<a name="table182073261196"></a>
<table><thead align="left"><tr id="row15182930101912"><th class="cellrowborder" valign="top" width="59.95%" id="mcps1.1.3.1.1"><p id="p5182330141913"><a name="p5182330141913"></a><a name="p5182330141913"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="40.050000000000004%" id="mcps1.1.3.1.2"><p id="p9182030141914"><a name="p9182030141914"></a><a name="p9182030141914"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row22071226161911"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p520772612199"><a name="p520772612199"></a><a name="p520772612199"></a>POST /v1.0/{project_id}/asset/status/publish</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1420711266190"><a name="p1420711266190"></a><a name="p1420711266190"></a><a href="媒资发布.md">媒资发布</a></p>
</td>
</tr>
<tr id="row8207112618193"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p52081326181918"><a name="p52081326181918"></a><a name="p52081326181918"></a>POST /v1.0/{project_id}/asset/status/unpublish</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p532932842013"><a name="p532932842013"></a><a name="p532932842013"></a><a href="媒资发布取消.md">媒资发布取消</a></p>
</td>
</tr>
<tr id="row1320812265196"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p1920811261192"><a name="p1920811261192"></a><a name="p1920811261192"></a>PUT /v1.0/{project_id}/asset/info</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p12328528132011"><a name="p12328528132011"></a><a name="p12328528132011"></a><a href="修改媒资属性.md">修改媒资属性</a></p>
</td>
</tr>
<tr id="row1220810263192"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p520872681915"><a name="p520872681915"></a><a name="p520872681915"></a>DELETE /v1.0/{project_id}/asset</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p19328172819209"><a name="p19328172819209"></a><a name="p19328172819209"></a><a href="删除媒资.md">删除媒资</a></p>
</td>
</tr>
<tr id="row1120813264196"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p3208826151911"><a name="p3208826151911"></a><a name="p3208826151911"></a>GET /v1.0/{project_id}/asset/info</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p15327028102020"><a name="p15327028102020"></a><a name="p15327028102020"></a><a href="查询媒资信息.md">查询媒资信息</a></p>
</td>
</tr>
<tr id="row1420817268196"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p6208326131916"><a name="p6208326131916"></a><a name="p6208326131916"></a>GET /v1.0/{project_id}/asset/details</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p532682822019"><a name="p532682822019"></a><a name="p532682822019"></a><a href="查询媒资详细信息.md">查询媒资详细信息</a></p>
</td>
</tr>
<tr id="row120952616199"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p11209182614198"><a name="p11209182614198"></a><a name="p11209182614198"></a>GET /v1.0/{project_id}/asset/list</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p203221228112013"><a name="p203221228112013"></a><a name="p203221228112013"></a><a href="查询媒资列表.md">查询媒资列表</a></p>
</td>
</tr>
</tbody>
</table>

## 媒资处理<a name="section1819719437223"></a>

<a name="table19855106231"></a>
<table><thead align="left"><tr id="row15685204142316"><th class="cellrowborder" valign="top" width="59.95%" id="mcps1.1.3.1.1"><p id="p0685124162320"><a name="p0685124162320"></a><a name="p0685124162320"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="40.050000000000004%" id="mcps1.1.3.1.2"><p id="p86856417238"><a name="p86856417238"></a><a name="p86856417238"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row165542143711"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p1963195823715"><a name="p1963195823715"></a><a name="p1963195823715"></a>PUT /v1.0/{project_id}/asset</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p56311658103712"><a name="p56311658103712"></a><a name="p56311658103712"></a><a href="视频更新.md">视频更新</a></p>
</td>
</tr>
<tr id="row19912452371"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p112931452123718"><a name="p112931452123718"></a><a name="p112931452123718"></a>POST /v1.0/{project_id}/asset/extract_audio</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p52931052193713"><a name="p52931052193713"></a><a name="p52931052193713"></a><a href="音频提取.md">音频提取</a></p>
</td>
</tr>
<tr id="row68563002313"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p148567022317"><a name="p148567022317"></a><a name="p148567022317"></a>POST /v1.0/{project_id}/asset/process</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1452516367231"><a name="p1452516367231"></a><a name="p1452516367231"></a><a href="视频处理.md">视频处理</a></p>
</td>
</tr>
<tr id="row8673163872920"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p567473852918"><a name="p567473852918"></a><a name="p567473852918"></a>DELETE /v1.0/{project_id}/asset/process</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p8674738102920"><a name="p8674738102920"></a><a name="p8674738102920"></a><a href="取消媒资转码任务.md">取消媒资转码任务</a></p>
</td>
</tr>
<tr id="row18864117163014"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p16864141714309"><a name="p16864141714309"></a><a name="p16864141714309"></a>DELETE /v1.0/{project_id}/asset/extract_audio</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1386481763010"><a name="p1386481763010"></a><a name="p1386481763010"></a><a href="取消提取音频任务.md">取消提取音频任务</a></p>
</td>
</tr>
<tr id="row326191817471"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p69839188472"><a name="p69839188472"></a><a name="p69839188472"></a>POST /v1.0/{project_id}/asset/review</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p198310186476"><a name="p198310186476"></a><a name="p198310186476"></a><a href="媒资审核.md">媒资审核</a></p>
</td>
</tr>
<tr id="row8558145913473"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0128109935_zh-cn_topic_0127939728_p757644710309"><a name="zh-cn_topic_0128109935_zh-cn_topic_0127939728_p757644710309"></a><a name="zh-cn_topic_0128109935_zh-cn_topic_0127939728_p757644710309"></a>PUT /v1.0/{project_id}/asset/cover</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p12558859194717"><a name="p12558859194717"></a><a name="p12558859194717"></a><a href="设置封面.md">设置封面</a></p>
</td>
</tr>
</tbody>
</table>

## 媒资分类<a name="section17774201872712"></a>

<a name="table1079032632712"></a>
<table><thead align="left"><tr id="row1189417296271"><th class="cellrowborder" valign="top" width="59.95%" id="mcps1.1.3.1.1"><p id="p489452917271"><a name="p489452917271"></a><a name="p489452917271"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="40.050000000000004%" id="mcps1.1.3.1.2"><p id="p789472911275"><a name="p789472911275"></a><a name="p789472911275"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row87911626182710"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p1979182632713"><a name="p1979182632713"></a><a name="p1979182632713"></a>POST /v1.0/{project_id}/asset/category</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p480085711272"><a name="p480085711272"></a><a name="p480085711272"></a><a href="创建媒资分类.md">创建媒资分类</a></p>
</td>
</tr>
<tr id="row0791182642711"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p197911226142714"><a name="p197911226142714"></a><a name="p197911226142714"></a>PUT /v1.0/{project_id}/asset/category</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p117998574277"><a name="p117998574277"></a><a name="p117998574277"></a><a href="修改媒资分类.md">修改媒资分类</a></p>
</td>
</tr>
<tr id="row27911826112720"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p8791202632719"><a name="p8791202632719"></a><a name="p8791202632719"></a>DELETE /v1.0/{project_id}/asset/category</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p13799457142718"><a name="p13799457142718"></a><a name="p13799457142718"></a><a href="删除媒资分类.md">删除媒资分类</a></p>
</td>
</tr>
<tr id="row1679132612279"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p7791152616278"><a name="p7791152616278"></a><a name="p7791152616278"></a>GET /v1.0/{project_id}/asset/category</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p479812578273"><a name="p479812578273"></a><a name="p479812578273"></a><a href="查询分类.md">查询分类</a></p>
</td>
</tr>
</tbody>
</table>

## 统计分析<a name="section373855542811"></a>

<a name="table1079750112910"></a>
<table><thead align="left"><tr id="row395925142918"><th class="cellrowborder" valign="top" width="59.95%" id="mcps1.1.3.1.1"><p id="p3959205142917"><a name="p3959205142917"></a><a name="p3959205142917"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="40.050000000000004%" id="mcps1.1.3.1.2"><p id="p1595910516297"><a name="p1595910516297"></a><a name="p1595910516297"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1179717072913"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p6797170142914"><a name="p6797170142914"></a><a name="p6797170142914"></a>GET /v1.0/{project_id}/asset/cdn-statistics</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p64564242299"><a name="p64564242299"></a><a name="p64564242299"></a><a href="查询CDN统计信息.md">查询CDN统计信息</a></p>
</td>
</tr>
<tr id="row1379715092915"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p197971806294"><a name="p197971806294"></a><a name="p197971806294"></a>GET /v1.0/{project_id}/asset/vod-statistics</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1645582422913"><a name="p1645582422913"></a><a name="p1645582422913"></a><a href="查询源站统计信息.md">查询源站统计信息</a></p>
</td>
</tr>
<tr id="row157981203295"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p1479817082918"><a name="p1479817082918"></a><a name="p1479817082918"></a>GET /v1.0/{project_id}/asset/top-statistics</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p1545416246297"><a name="p1545416246297"></a><a name="p1545416246297"></a><a href="查询TopN媒资信息.md">查询TopN视频信息</a></p>
</td>
</tr>
</tbody>
</table>

## 查询密钥<a name="section0232161773316"></a>

<a name="table796242413344"></a>
<table><thead align="left"><tr id="row1396252417347"><th class="cellrowborder" valign="top" width="59.95%" id="mcps1.1.3.1.1"><p id="p2962102423414"><a name="p2962102423414"></a><a name="p2962102423414"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="40.050000000000004%" id="mcps1.1.3.1.2"><p id="p1196362419349"><a name="p1196362419349"></a><a name="p1196362419349"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1496362493418"><td class="cellrowborder" valign="top" width="59.95%" headers="mcps1.1.3.1.1 "><p id="p66303377349"><a name="p66303377349"></a><a name="p66303377349"></a>GET /v1.0/{project_id}/asset/ciphers</p>
</td>
<td class="cellrowborder" valign="top" width="40.050000000000004%" headers="mcps1.1.3.1.2 "><p id="p463083719343"><a name="p463083719343"></a><a name="p463083719343"></a><a href="密钥查询接口.md">查询密钥</a></p>
</td>
</tr>
</tbody>
</table>

