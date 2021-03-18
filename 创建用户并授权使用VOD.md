# 创建用户并授权使用VOD<a name="vod010012"></a>

如果您需要对您所拥有的VOD进行精细的权限管理，您可以使用[统一身份认证服务](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)（Identity and Access Management，简称IAM），通过IAM，您可以：

-   根据企业的业务组织，在您的华为云账号中，给企业中不同职能部门的员工创建IAM用户，让员工拥有唯一安全凭证，并使用VOD资源。
-   根据企业用户的职能，设置不同的访问权限，以达到用户之间的权限隔离。
-   将VOD资源委托给更专业、高效的其他华为云账号或者云服务，这些账号或者云服务可以根据权限进行代运维。

如果华为云账号已经能满足您的要求，不需要创建独立的IAM用户，您可以跳过本章节，不影响您使用VOD服务的其它功能。

本章节为您介绍对用户授权的方法，操作流程如[图1](#fig1354612376295)所示。

## 前提条件<a name="section1483264620406"></a>

给用户组授权之前，请您了解用户组可以添加的VOD系统权限，并结合实际需求进行选择，VOD支持的系统权限，请参见：[VOD系统权限](https://support.huaweicloud.com/productdesc-vod/vod030006.html)。

## 示例流程<a name="section8161102163310"></a>

**图 1**  给用户授权VOD只读权限流程<a name="fig1354612376295"></a>  
![](figures/给用户授权VOD只读权限流程.png "给用户授权VOD只读权限流程")

1.  <a name="li12825948184211"></a>[创建用户组并授权](https://support.huaweicloud.com/usermanual-iam/iam_03_0001.html)

    在IAM控制台创建用户组，并授予VOD只读权限“VOD Guest”。

2.  [创建用户并加入用户组](https://support.huaweicloud.com/usermanual-iam/iam_02_0001.html)

    在IAM控制台创建用户，并将其加入[1](#li12825948184211)中创建的用户组。

3.  [用户登录](https://support.huaweicloud.com/usermanual-iam/iam_01_0552.html)并验证权限

    新创建的用户登录控制台，切换至授权区域，验证权限：

    -   在“服务列表”中选择视频点播服务，进入“音视频审核”界面，若提示权限不足，表示“VOD Guest”已生效。
    -   在“服务列表”中选择除弹性云服务器外的任一服务，若提示权限不足，表示“VOD Guest”已生效。


## 创建媒资隔离的用户<a name="section167672617121"></a>

视频点播提供了VOD Administrator、VOD Operator、VOD Guest、VOD Group Administrator、VOD Group Operator、VOD Group Guest六个系统策略，具体请参考[产品介绍-权限管理](https://support.huaweicloud.com/productdesc-vod/vod030006.html)。其中前三个系统策略仅能进行操作权限的划分，若您还需要对视频点播中存储的媒资进行隔离，建议您使用后三个系统策略，它们既支持操作权限划分，也支持媒资隔离。媒资隔离是指仅同组内的用户能访问或管理该组其他用户创建的媒资。

媒资隔离示例如[表1](#table1128611499308)所示。

**表 1**  账号权限配置建议

<a name="table1128611499308"></a>
<table><thead align="left"><tr id="row928818497301"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p628894913306"><a name="p628894913306"></a><a name="p628894913306"></a>策略组</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p17893164163112"><a name="p17893164163112"></a><a name="p17893164163112"></a>用户A（管理账号）</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p11288144916304"><a name="p11288144916304"></a><a name="p11288144916304"></a>用户B（上传账号）</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p20288164973020"><a name="p20288164973020"></a><a name="p20288164973020"></a>用户C（观看账号）</p>
</th>
</tr>
</thead>
<tbody><tr id="row528854923017"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p11957132043115"><a name="p11957132043115"></a><a name="p11957132043115"></a>VOD Group Administrator</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p8650135023114"><a name="p8650135023114"></a><a name="p8650135023114"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p156731445143110"><a name="p156731445143110"></a><a name="p156731445143110"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1128916493305"><a name="p1128916493305"></a><a name="p1128916493305"></a>-</p>
</td>
</tr>
<tr id="row3289124953019"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p112891499305"><a name="p112891499305"></a><a name="p112891499305"></a>VOD Group Operator</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p20110934182516"><a name="p20110934182516"></a><a name="p20110934182516"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p1159204203114"><a name="p1159204203114"></a><a name="p1159204203114"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p628924983018"><a name="p628924983018"></a><a name="p628924983018"></a>-</p>
</td>
</tr>
<tr id="row52891249103013"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1828954943019"><a name="p1828954943019"></a><a name="p1828954943019"></a>VOD Group Guest</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p121101734152511"><a name="p121101734152511"></a><a name="p121101734152511"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p359092533215"><a name="p359092533215"></a><a name="p359092533215"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p104101538113114"><a name="p104101538113114"></a><a name="p104101538113114"></a>√</p>
</td>
</tr>
</tbody>
</table>

以上三种策略组，不管是低权限的账户还是高权限的账户，都只能操作本组内用户创建的媒资，达到了媒资隔离的效果，即用户A、B、C只能访问自己组内的媒资。

若用户A需要能操作用户B创建的媒资，则用户A需要加入B所在的VOD Group Operator策略组。

