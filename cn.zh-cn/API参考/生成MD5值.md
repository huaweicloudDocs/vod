# 生成MD5值<a name="vod_04_0212"></a>

## 媒资上传和更新<a name="section1556644615814"></a>

调用[创建媒资：上传方式](https://support.huaweicloud.com/api-vod/vod_04_0196.html)和[视频更新](https://support.huaweicloud.com/api-vod/vod_04_0207.html)接口时，可以通过“video\_md5“设置媒资文件的MD5值。设置后，OBS会对媒资的MD5值进行检验，具体可参考[设置对象属性](https://support.huaweicloud.com/sdk-ios-devg-obs/obs_27_0405.html)。

该MD5值是经过标准的MD5哈希算法计算后，再进行base64编码的。示例代码如下所示：

```
import org.apache.commons.codec.binary.Base64;

import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;

import java.security.DigestInputStream;
import java.security.MessageDigest;
import java.security.NoSuchAlgorithmException;


public class VodDemoObsCheckMd5 {
    public String md5Generate4ObsCheck(String fileUrl)
        throws IOException, NoSuchAlgorithmException {
        String md5Content = null;

        if ((fileUrl != null) && (fileUrl.length() != 0)) {
            File file = new File(fileUrl);

            if (!file.exists()) {
                System.out.println("文件不存在");
            } else if (file.isDirectory()) {
                System.out.println(file.getCanonicalPath() + "是一个目录,无法计算");
            } else {
                FileInputStream fis = new FileInputStream(file);
                DigestInputStream dis = new DigestInputStream(fis,
                        MessageDigest.getInstance("MD5"));
                byte[] buffer = new byte[8192];

                while (dis.read(buffer) > 0) {
                }

                md5Content = new String(Base64.encodeBase64(
                            dis.getMessageDigest().digest()));
                fis.getChannel().position(0L);
                System.out.println("该文件MD5为： " + md5Content);
                fis.close();
            }
        } else {
            System.out.println("缺少文件名");
        }

        return md5Content;
    }
}

```

## 上传校验<a name="section575102165412"></a>

调用[上传检验](https://support.huaweicloud.com/api-vod/vod_04_0050.html)接口时，点播服务会根据媒资的MD5值来检查是否已有重复的媒资文件。MD5值的生成方式是取媒资文件的1024字节，并进行MD5计算。具体MD5计算的实现您可以[下载](https://support.huaweicloud.com/ssdk-vod/vod_05_0074.html)点播服务端SDK，引入“cloud-java-sdk-vod-2.0.4.jar“进行开发，示例代码如下所示：

```
import com.huawei.common.util.Md5Utils;
import java.io.File;
import java.io.IOException;
import java.security.NoSuchAlgorithmException;

public class VodDemoDuplicateCheckMd5 {
    public String md5Generate4DuplicateCheck(String fileUrl)
        throws IOException, NoSuchAlgorithmException {
        String md5Content = null;

        if ((fileUrl != null) && (fileUrl.length() != 0)) {
            File file = new File(fileUrl);

            if (!file.exists()) {
                System.out.println("文件不存在");
            } else if (file.isDirectory()) {
                System.out.println(file.getCanonicalPath() + "是一个目录,无法计算");
            } else {
                md5Content = Md5Utils.computeMd5ByFile(fileUrl);
            }
        } else {
            System.out.println("缺少文件名");
        }

        return md5Content;
    }
}
```

