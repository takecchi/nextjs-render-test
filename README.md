# nextjs-render-test
SSG,SSR,RSC,RCCの動作を確認するためのリポジトリ。

コードはこちらを参考にさせていただいています。
[【Next.js】App RouterはAWS Amplify Hostingに何をもたらすのか？](https://zenn.dev/ototrip/articles/tech-nextjs-approuter-1)

## How to use

```bash
npm install
npm run build
npm run start
```
ローカルで立ち上がります。

## OpenNextでAWS向けビルド
以下のコマンドでOpenNextを使用したAWS向けのビルドが出来ます。

```bash
npx open-next build
```

## AWSにデプロイする(SSTを使用する方法)
openNext+SSTを使用したデプロイ方法になります。

### 事前準備
AWSからクレデンシャルを払い出しておくこと。

### デプロイ
```bash
npx sst deploy
```
- 実行することでAWS上に自動的にサービスが構成されます。 `./.sst`
- OpenNextを使用したAWS向けのビルドが行われます。 `./.open-next`
- CloudFormationで管理可能。
