名前: ウォッチタワー
説明: ウォッチタワーの理解と使用方法
---

# ウォッチタワーのライトニング

> クレジット: https://blog.summerofbitcoin.org/bitcoin-lightning-and-the-eye-of-satoshi-watchtower-revolutionizing-transactions-and-security//

## ウォッチタワーはどのように機能するのか？

ライトニングネットワークエコシステムの重要な部分であるウォッチタワーは、ユーザーのライトニングチャネルに追加の保護を提供します。その主な責任は、チャネルの健全性を監視し、一方のチャネルパーティが他方を詐欺しようとした場合に介入することです。

では、ウォッチタワーはチャネルが侵害されたかどうかをどのように判断するのでしょうか？ウォッチタワーは、クライアント（チャネルの一方のパーティ）から必要な情報を受け取り、適切に侵害を特定し、対応するために使用します。最新のトランザクションの詳細、現在のチャネルの状態、およびペナルティトランザクションを作成するために必要な情報が、この情報に頻繁に含まれます。クライアントは、プライバシーと機密性を保護するために、データを暗号化することがあります。これにより、ウォッチタワーはデータを受け取ったとしても、実際に侵害が発生しない限り、暗号化されたデータを復号化することはできません。この暗号化システムにより、クライアントのプライバシーが保護され、ウォッチタワーが許可なくプライベートデータにアクセスすることが防止されます。

## 自分自身のサトシの目を設定して貢献を開始する方法

サトシの目（[RUST-TEOS](https://github.com/talaia-labs/rust-teos?ref=blog.summerofbitcoin.org)）は、[BOLT 13](https://github.com/sr-gi/bolt13/blob/master/13-watchtowers.md?ref=blog.summerofbitcoin.org)に準拠した非保管型のライトニングウォッチタワーです。主なコンポーネントは次のとおりです。

1. teos: CLIとタワーのサーバーサイドのコア機能を含みます。このクレートがビルドされると、teosdとteos-cliの2つのバイナリが生成されます。

2. teos-common: サーバーサイドとクライアントサイドの共有機能を含みます（クライアントの作成に役立ちます）。

タワーを正常に実行するには、teosdコマンドでタワーを実行する前にbitcoindを実行する必要があります。これらのコマンドを実行する前に、bitcoin.confファイルを設定する必要があります。以下はその手順です。

1. ソースからBitcoin Coreをインストールするか、ダウンロードします。ダウンロード後、bitcoin.confファイルをBitcoin Coreのユーザーディレクトリに配置します。ファイルの配置場所は使用しているオペレーティングシステムによって異なるため、詳細についてはこのリンクを参照してください。

2. ファイルを作成する場所を特定した後、次のオプションを追加します。

'''
#RPC
server=1
rpcuser=<your-user>
rpcpassword=<your-password>

#chain
regtest=1
'''

* server: RPCリクエスト用
* rpcuserとrpcpassword: RPCクライアントがサーバーに認証するためのもの
* regtest: 開発を計画している場合には必要ありませんが、便利です。

rpcuserとrpcpasswordは自分で選択する必要があります。引用符なしで書かれている必要があります。例：

'''
rpcuser=aniketh
rpcpassword=strongpassword
'''

これで、bitcoindを実行するとノードが起動するはずです。

1. タワーの部分については、まずソースからteosをインストールする必要があります。このリンクに記載されている手順に従ってください。
2. teosをシステムに正常にインストールし、テストを実行した後、最後のステップであるteosユーザーディレクトリにteos.tomlファイルを設定することができます。ファイルは、ホームフォルダの下に.teosという名前のフォルダに配置する必要があります。つまり、Linuxの場合は/home/<your-username>/.teosです。場所を見つけたら、teos.tomlファイルを作成し、bitcoindで変更した内容に対応するこれらのオプションを設定します。

'''
#bitcoind
btc_network = "regtest"
btc_rpc_user = <your-user>
btc_rpc_password = <your-password>
'''

ここで、ユーザー名とパスワードは引用符で囲んで書かれる必要があることに注意してください。つまり、前述の例では次のようになります。

'''
btc_rpc_user = "aniketh"
btc_rpc_password = "strongpassword"
'''

これを行ったら、towerを実行する準備が整いました。regtestで実行しているため、最初にtowerが接続するときにはビットコインのテストネットワークでブロックが採掘されない可能性があります（もし採掘されている場合は、何かが間違っています）。towerはbitcoindから最新の100ブロックの内部キャッシュを構築するため、初回実行時には次のエラーが発生する場合があります。

> ERROR [teosd] Not enough blocks to start the tower (required: 100). Mine at least 100 more

regtestで実行しているため、他のネットワーク（メインネットやテストネットなど）で通常見られる10分間の中央時間を待つ必要はなく、RPCコマンドを発行してブロックを採掘することができます。bitcoin-cli helpを確認し、ブロックを採掘する方法を調べてください。ヘルプが必要な場合は、この記事を参照してください。

![image](assets\2.png)

以上で、towerの実行が成功しました。おめでとうございます。 🎉

https://blog.summerofbitcoin.org/bitcoin-lightning-and-the-eye-of-satoshi-watchtower-revolutionizing-transactions-and-security//