[下载](https://www.123pan.com/s/QyezVv-QHJph.html)

packagename:
1.3.4: `org.tvp.kirikiri2_free_10304`
改为: `org.tvp.kirikiri2_free_134`
1.3.9: `org.tvp.kirikiri2_free_10309`
改为: `org.tvp.kirikiri2_free_139`

AndroidManifest.xml 修改:
由于安卓14无法安装TargetSDK低于23的应用
```   
<uses-sdk  android:minSdkVersion="11" />
```
改为
```   
<uses-sdk  android:minSdkVersion="11"
           android:targetSdkVersion="30" />
```
manifest清单添加安卓11新存储权限以解决读写公共目录问题。


```
<application
        android:label="吉里吉里2模拟器 1.3.9"
        android:icon="@drawable/ic_launcher"
        android:allowBackup="true"
        android:resizeableActivity="true">
```
改为
```
<application
        android:label="吉里吉里2模拟器 1.3.9"
        android:icon="@drawable/ic_launcher"
        android:allowBackup="true"
        android:resizeableActivity="true"
        android:requestLegacyExternalStorage="true">
```