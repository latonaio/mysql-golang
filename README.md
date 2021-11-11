# mysql-golang
mysql-golang は、Golang で動作する(マイクロサービス)ランタイムにおける、MySQL の適用方法を記載したレポジトリです。  
Golangの場合、ライブラリの依存関係を共通レポジトリで構築できないため、AIONでは、Golangランタイムにおける MySQL の適用をマイクロサービス毎に定義しています。  
他方、AIONでは、Nodejsランタイム、Pythonランタイム で MySQL を使用する場合、原則としてマイクロサービス毎に MySQL を適用せずに、エッジコンピューティング環境毎に共通定義することとし、libraryとして共通化しております。  
詳細については、[mysql-nodejs-client](https://github.com/latonaio/mysql-nodejs-client)、[mysql-python-client](https://github.com/latonaio/mysql-python-client)を参照してください。

## 動作環境

* OS: Linux  
* CPU: ARM/AMD/Intel  
* Golang Runtime  

## Golang(マイクロサービス)ランタイム における MySQL の適用方法  

Golang(マイクロサービスランタイム)環境で MySQL を適用する場合は、go.modに以下のように記載します。  
```
module MODULE-NAME

go 1.17

require (
	github.com/go-sql-driver/mysql v1.6.0
	gorm.io/gorm v1.22.2
)
```