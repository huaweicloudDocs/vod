# HTTPS证书要求<a name="vod010034"></a>

HTTPS配置仅支持PEM格式的证书/私钥内容上传，针对不同的证书颁发机构，对证书/私钥内容的上传有不同的要求。

## Root CA机构颁发的证书<a name="zh-cn_topic_0064907759_section47392574183850"></a>

Root CA机构颁发的证书是一份完整的证书，配置HTTPS时，仅上传该证书即可。

通过记事本打开\*.PEM格式的证书文件，可以查看到类似[图1](#zh-cn_topic_0064907759_fig62782747144849)所示的全部证书信息。

PEM格式证书：

-   以证书链“-----BEGIN CERTIFICATE-----”开头，以证书链“-----END CERTIFICATE-----”结尾。
-   证书链之间的内容，要求每行64个字符，最后一行允许不足64个字符。
-   证书内容不包含空格。

**图 1**  PEM格式证书<a name="zh-cn_topic_0064907759_fig62782747144849"></a>  
![](figures/PEM格式证书.png "PEM格式证书")

## 中级CA机构颁发的证书<a name="zh-cn_topic_0064907759_section23934614192754"></a>

中级机构颁发的证书文件包含多份证书，配置HTTPS时，需要将所有证书拼接在一起组成一份完整的证书后再上传。拼接后的证书类似[图2](#zh-cn_topic_0064907759_fig26971979202252)。

通过记事本打开所有\*.PEM格式的证书文件，将**服务器证书**放在首位，再放置**中间证书**。一般情况下，机构在颁发证书的时候会有对应说明，请注意查阅相关规则。通用的规则如下：

-   证书之间没有空行。
-   证书链的格式如下：

    -----BEGIN CERTIFICATE-----

    -----END CERTIFICATE-----

    -----BEGIN CERTIFICATE-----

    -----END CERTIFICATE-----


**图 2**  拼接后的PEM证书<a name="zh-cn_topic_0064907759_fig26971979202252"></a>  
![](figures/拼接后的PEM证书.png "拼接后的PEM证书")

## RSA私钥格式要求<a name="zh-cn_topic_0064907759_section28051642201353"></a>

PEM格式的文件可以存放证书或私钥，如果\*.PEM只包含私钥，一般用\*.KEY代替。

通过记事本打开\*.PEM或\*.KEY的私钥文件，可以查看到类似[图3](#zh-cn_topic_0064907759_fig4908845816121)所示的全部私钥信息。

RSA格式私钥：

-   以证书链“-----BEGIN RSA PRIVATE KEY-----”开头，以证书链“-----END RSA PRIVATE KEY-----”结尾。
-   证书链之间的内容，要求每行64个字符，最后一行允许不足64个字符。
-   证书内容不包含空格。

**图 3**  RSA格式私钥<a name="zh-cn_topic_0064907759_fig4908845816121"></a>  
![](figures/RSA格式私钥.png "RSA格式私钥")

当私钥的证书链带有“-----BEGIN PRIVATE KEY-----, -----END PRIVATE KEY-----”或者“-----BEGIN ENCRYPTED PRIVATE KEY-----, -----END ENCRYPTED PRIVATE KEY-----”信息时，需要使用OpenSSL工具执行以下命令进行转换：

```
openssl rsa -in old_key.pem -out new_key.pem
```

## 格式转换<a name="zh-cn_topic_0064907759_section6645502812116"></a>

配置HTTPS仅支持PEM格式的证书/私钥，其他格式均不支持。其他格式的证书/私钥需要转换成PEM格式，建议通过[OpenSSL](https://www.openssl.org/source/)工具进行转换。下面是几种比较流行的证书格式转换为PEM格式的方法。

以下示例均假设转换前证书名为old\_certificate，私钥名为old\_key，转换后证书名为new\_certificate，私钥文件名为new\_key。

-   **DER转换为PEM**

    ```
    openssl x509 -inform der -in old_certificate.cer -out new_certificate.pem
    openssl rsa -inform DER -outform pem -in old_key.der -out new_key.pem
    ```


-   **P7B转换为PEM**

    ```
    openssl pkcs7 -print_certs -in old_certificate.p7b -out new_certificate.cer
    ```


-   **PFX转换为PEM**

    ```
    openssl pkcs12 -in old_certificat.pfx -nokeys -out new_certificate.pem
    openssl pkcs12 -in old_certificat.pfx -nocerts -out new_key.pem
    ```


