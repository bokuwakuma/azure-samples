# spring-boot-azure
Azure環境にデプロイしてみる

- 参考：[Spring Boot on Microsoft Azure](https://qiita.com/kikutaro/items/251aebc572794105a524)

### step1
まずはControllerを作成して普通に動作確認

### step2
azure-webapp-maven-pluginの設定を追加
```xml:pom.xml

```

### トラブルシューティング
- Azure CLIのインストール

- 以下のエラー１
```
[ERROR] Failed to execute goal com.microsoft.azure:azure-webapp-maven-plugin:1.6.0:deploy (default-cli) on project spring-boot-azure: No runtime related configuration is specified in pom.xml. For V1 schema version, please use <javaVersion>, <linuxRuntime> or <containerSettings>, For V2 schema version, please use <runtime>. -> [Help 1]
```
 - Runtime省略しちゃダメなのね。

- 以下のエラー２
```
[ERROR] Failed to execute goal com.microsoft.azure:azure-webapp-maven-plugin:1.6.0:deploy (default-cli) on project spring-boot-azure: java.io.IOException: Failed to authenticate with proxy -> [Help 1]
```
 - 出たproxy・・・
