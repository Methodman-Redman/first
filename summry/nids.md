# nids

## money

https://www.softwaretestinghelp.com/intrusion-detection-systems/
https://www.gartner.com/reviews/market/intrusion-prevention-systems

Palo Alto Networks  
McAfee Network Security Platform  
Trend Micro TippingPoint NGIPS  
FireEye Network Security (NX)  
Hillstone S-Series Intrusion Prevention System  
Fidelis Network  
NSFOCUS IPS  
Network Intelligent Protection (NIP) System  

## no money

snort  
シグネチャベース  
異常ベース  
の2つの検出方法を使用  
OSフィンガープリント  
ポートスキャン  
SMBプローブ  
および他の多くの異なる攻撃を検出できます。  

suricata
シグネチャベース  
異常ベースの検出方法  
Snortのデータ構造と互換性があり、利便性を高めるためにSuricata内にSnortポリシーベースを実装することもできます。  
ネットワーク侵入検知にとどまらず、TLS 証明書、HTTP 要求、および DNS トランザクションの検査  

Zeek(旧Bro)  
シグネチャベース  
異常ベースの検出方法  
HTTP、DNS、SNMP トラフィック、FTP など、さまざまな OSI レイヤーのさまざまなサービスを追跡する機能を提供します。  

 OpenWIPS-ng  
 ワイヤレスネットワークに特化した無料のオープンソースNIDSであり、WIPSはワイヤレス侵入防止システムの略  
 
# hids

## money

https://www.dnsstuff.com/host-based-intrusion-detection-systems　　 
SolarWinds Security Event Manager  
SolarWinds Papertrail  
ManageEngine EventLog Analyzer  
Splunk  

## no money
https://nagasaki-noc.ne.jp/introduction-5-popular-open-source-hids-systems
ossec  
シグニチャおよび異常検出方法  
ログ分析、ファイル整合性チェック、ポリシーモニタリング、ルートキット検出、およびアクティビティ応答を実行  
Windows、さまざまなLinuxディストリビューション、およびMacOS  
リアルタイムで通知される  
  
Tripwire  
Linux  
正常な状態でのシステムのスナップショット（ベースラインデータベース）を内部データベースとして保持し、現在の状態でのシステムのスナップショットと比較することで改ざんを検知  
リアルタイムで通知されない  
ファイルの内容が変更された  
ファイルやディレクトリが追加された  
ファイルやディレクトリが削除された  
ファイルやディレクトリのオーナー・パーミッションが変更された  


Samhain  
異常検出方法  
リアルタイムで通知される  
Unix、Linux、Cygwin / Windows POSIXシステム  
ファイル整合性チェック  
ログファイル監視/分析  
ポート監視  
不正な SUID 実行可能ファイルの検出  


セキュリティオニオン  
侵入検知・エンドポイント監視などを目的に作られてディストリビューション  

## signature anomary
http://www.sql-master.net/articles/SQL1621.html

## snort siem
https://www.web-dev-qa-db-ja.com/ja/snort/snort%E3%81%AA%E3%81%A9%E3%81%AE%E3%82%BB%E3%83%B3%E3%82%B5%E3%83%BC%E3%82%92alienvault-siem%E3%81%AB%E6%8E%A5%E7%B6%9A%E3%81%99%E3%82%8B%E3%81%AB%E3%81%AF%E3%81%A9%E3%81%86%E3%81%99%E3%82%8C%E3%81%B0%E3%82%88%E3%81%84%E3%81%A7%E3%81%99%E3%81%8B%EF%BC%9F/l958421179/amp/  

## ossec siem
https://qiita.com/Diavolo/items/d010020d35b46c556d60
