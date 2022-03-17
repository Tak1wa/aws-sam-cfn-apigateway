# aws-sam-cfn-apigateway

## step

- Route53ホストゾーン作成。ホストゾーンIDを取得しておく
- mTLS用に証明書やら作成。CodeBuildロールからアクセス可能なS3へアップロードしておく
- CodePipeline構築

## CodePipeline.ParameterOverrides Sample

```
{
    "ApiName": "iwasa-api", 
    "StageName": "iwasa-stage",
     "HostedZoneId": "Z07463711IS7W792VK625", 
     "CustomDomainName": "apihoge.tak1wa.com", 
     "TrustStoreS3Uri": "s3://20220317mtls/RootCA.pem"
}
```