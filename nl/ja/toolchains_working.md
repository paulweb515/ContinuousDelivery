---

copyright:
  years: 2015, 2019

lastupdated: "2019-2-8"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# ツールチェーンの作成
{: #toolchains_getting_started}

*ツールチェーン*は、開発、デプロイメント、運用の作業をサポートするツール統合のセットです。 ツールチェーンの集合的な機能は、個々のツール統合を合わせたものより優れています。
{: shortdesc}

{{site.data.keyword.Bluemix}} の Public 環境と Dedicated 環境で、オープンなツールチェーンが使用可能です。 ツールチェーンの作成方法には、テンプレートを使用する方法と、アプリから作成する方法の 2 とおりがあります。

各ツールチェーンは、特定のリソース・グループまたは組織に関連付けられています。 ツールチェーンがリソース・グループに関連付けられている場合、ツールチェーン・リソースまたはそれを含むリソース・グループに対して Identity and Access Management (IAM) ビューアー・アクセス権を持つすべてのユーザーがツールチェーンにアクセスできます。 ツールチェーンが組織に関連付けられている場合、その組織のメンバーである任意のユーザーを、関連するツールチェーンのアクセス制御リストに追加することができます。 Cloud Foundry 組織内のツールチェーンのアクセス制御について詳しくは、[Cloud Foundry の組織内のツールチェーンへのアクセスの管理](/docs/services/ContinuousDelivery?topic=ContinuousDelivery-toolchains-using#managing_access_orgs){: new_window}を参照してください。 リソース・グループ内のツールチェーンのアクセス制御について詳しくは、[リソース・グループ内のツールチェーンへのアクセスの管理](/docs/services/ContinuousDelivery?topic=ContinuousDelivery-toolchains-using#managing_access_resource_groups){: new_window}を参照してください。

##テンプレートからのツールチェーンの作成   
{: #creating_a_toolchain_from_a_template}

特定のツール統合のセットを含む[ツールチェーンを作成する ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://cloud.ibm.com/devops/create){: new_window} ための開始点としてテンプレートを使用できます。 テンプレートの使用方法について詳しくは、[IBM Cloud Garage Method ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud/garage/category/tools){:new_window} を参照してください。

1. {{site.data.keyword.Bluemix_notm}} Public を使用する場合、[{{site.data.keyword.Bluemix_notm}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://cloud.ibm.com){:new_window} にログインします。
1. {{site.data.keyword.Bluemix_notm}} Dedicated を使用する場合、{{site.data.keyword.Bluemix_notm}} の Dedicated 環境にログインします。
1. {{site.data.keyword.Bluemix_notm}} メニュー・バーのメニューから、**「DevOps」**をクリックします。
1. DevOps ダッシュボードの**「ツールチェーン」**ページで、**「ツールチェーンの作成 (Create a Toolchain)」**をクリックします。
1. **「ツールチェーンの作成 (Create a Toolchain)」**ページで、ツールチェーン・テンプレートをクリックします。
1. 作成しようとしているツールチェーンの図を確認します。 この図は、ツールチェーン内の各ツール統合とそのライフサイクル・フェーズを示しています。

 一部のツールチェーン・テンプレートには、同じツール統合の複数のインスタンスが含まれています。 例えば、{{site.data.keyword.Bluemix_notm}} Public の Microservices ツールチェーン・テンプレートには、GitHub の 3 つのインスタンスと Delivery Pipeline の 3 つのインスタンス (3 つのマイクロサービスのそれぞれに対して 1 つずつ) が含まれています。
 {: tip}

 次のイメージの図はその例です。 ツールチェーンを作成すると、ツールチェーンを構成する各ツール統合がこの図に表示されます。![ツールチェーンの図](images/toolchain_diagram2.png)

1. ツールチェーン設定のデフォルト情報を確認します。

 * ツールチェーンの名前は、そのツールチェーンを {{site.data.keyword.Bluemix_notm}} 内で識別するためのものです。 別の名前を使用する場合は、ツールチェーンの名前を変更します。
 * ツールチェーンを作成する対象の地域。 別の地域を利用する場合は、選択可能な地域のリストから選んでください。
 * ツールチェーンを作成する対象のリソース・グループまたは組織。 リンクをクリックして、リソース・グループと組織の選択を切り替えます。 別のリソース・グループまたは組織を利用する場合は、選択可能なリソース・グループまたは組織のリストから選んでください。
 
   リソース・グループは、米国南部、米国東部、英国、ドイツ、および東京領域で利用可能です。 Cloud Foundry の組織は、米国南部、英国およびドイツ地域でサポートされています。
   {: important}

1. 「ツール統合 (Tool Integrations)」セクションで、ツールチェーンに構成する各ツール統合を選択します。 いくつかのツール統合は、構成を必要としません。 ツール統合の構成については、[ツール統合の構成](/docs/services/ContinuousDelivery?topic=ContinuousDelivery-integrations){: new_window}を参照してください。
1. **「作成」**をクリックします。 以下のようにいくつかのステップが自動的に実行されて、ツールチェーンがセットアップされます。 セットアップされるツール統合は、どのツールチェーン・テンプレートを選択したのか、また、{{site.data.keyword.Bluemix_notm}} Public と {{site.data.keyword.Bluemix_notm}} Dedicated のどちらを使用しているのかによって異なります。 例えば、Microservices ツールチェーンを {{site.data.keyword.Bluemix_notm}} Public で作成する場合、以下のステップが実行されます。

 * ツールチェーンが作成されます。
 * Delivery Pipeline を構成した場合は、パイプラインが作成されて起動します。
 * Sauce Labs を構成した場合は、パイプラインに Sauce Labs テスト・ジョブを追加するようにツールチェーンがセットアップされます。
 * PagerDuty を構成した場合は、指定した PagerDuty サービスにアラート通知を送信するようにツールチェーンがセットアップされます。
 * Slack を構成した場合は、指定した Slack チャネルにデプロイメント状況に関する通知を送信するようにツールチェーンがセットアップされます。
 * GitHub などのソース・コード・ツール統合を構成した場合、サンプル GitHub リポジトリーが GitHub アカウントに複製されます。


##アプリからのツールチェーンの作成
{: #creating_a_toolchain_from_an_app}

アプリからツールチェーンを作成することができます。 ツールチェーンは、継続的な開発、デプロイメント、モニターなどをサポートすることができ、アプリと関連付けられます。 各アプリをツールチェーンと関連付けることができます。 ツールチェーンの GitHub リポジトリーまたは {{site.data.keyword.ghe_short}} リポジトリーに変更をプッシュすると、パイプラインは自動的にアプリをビルドしてデプロイします。

独自のコード・リポジトリーを使用してアプリを作成した場合は、アプリの詳細ページで**「DevOps ツールチェーンへの接続 (Connect to DevOps toolchain)」**をクリックします。 次いで、[独自のコード・リポジトリーからアプリを作成する](/docs/apps?topic=creating-apps-tutorial-byoc#tutorial-byoc)に記載されている手順を実行します。
{: note}

1. スターター・キットを使用をしてアプリを作成した場合は、アプリの詳細ページで**「クラウドにデプロイ (Deploy to cloud)」**をクリックします。 {{site.data.keyword.Bluemix_notm}} Public を使用する場合、アプリは、アプリ・スターター・コードが取り込まれた新規 GitHub リポジトリーからの継続的デリバリー用に構成されます。 {{site.data.keyword.Bluemix_notm}} Dedicated を使用する場合、アプリは、アプリ・スターター・コードが取り込まれた新規 GitHub リポジトリーまたは {{site.data.keyword.ghe_short}} リポジトリーからの継続的デリバリー用に構成されます。
1. ツールチェーン作成ページで、作成しようとしているツールチェーンの図を確認します。 この図は、ツールチェーン内の各ツール統合とそのライフサイクル・フェーズを示しています。
1. ツールチェーン設定のデフォルト情報を確認します。 ツールチェーンの名前は、そのツールチェーンを {{site.data.keyword.Bluemix_notm}} 内で識別するためのものです。 別の名前を使用する場合は、ツールチェーンの名前を変更します。
1. 「ツール統合 (Tool Integrations)」セクションで、ツールチェーンに構成する各ツール統合を選択します。 いくつかのツール統合は、構成を必要としません。 ツール統合の構成については、[ツール統合の構成](/docs/services/ContinuousDelivery?topic=ContinuousDelivery-integrations){: new_window}を参照してください。
1. **「作成」**をクリックします。 以下のようにいくつかのステップが自動的に実行されて、ツールチェーンがセットアップされます。 セットアップされるツール統合は、{{site.data.keyword.Bluemix_notm}} Public と {{site.data.keyword.Bluemix_notm}} Dedicated のどちらでツールチェーンを使用するのかによって異なります。 例えば、{{site.data.keyword.Bluemix_notm}} Public でアプリからツールチェーンを作成する場合、以下のステップが実行されます。

 * ツールチェーンが作成されます。
 * Delivery Pipeline を構成した場合は、パイプラインが作成されて起動します。
 * GitHub を構成した場合は、GitHub アカウントにサンプル GitHub リポジトリーが複製されます。


##ツールチェーンの表示
{: #viewing_a_toolchain}

ツールチェーンとそのツール統合を構成した後、ツールチェーンのビジュアル表示を確認することができます。

アプリの詳細ページから**「ツールチェーンの表示」**をクリックすることにより、アプリからツールチェーンを表示することができます。
{: tip}

1. DevOps ダッシュボードの**「ツールチェーン」**ページで、**「リソース・グループ」**または**「Cloud Foundry 組織」**をクリックします。 選択したリソース・グループまたは Cloud Foundry 組織内に含まれるすべてのツールチェーンが表示されます。 表示するツールチェーンをクリックして、「概要」ページを開きます。 あるいは、アプリの「概要」ページの「継続的デリバリー」カードで、**「ツールチェーンの表示」**をクリックします。 次に、**「概要」**をクリックします。
2. ツールチェーン内にあるツール統合にアクセスするには、ツールをクリックします。

 GitHub リポジトリー、{{site.data.keyword.ghe_short}} リポジトリー、または Git リポジトリーが複数ある場合、各リポジトリーはそれぞれ固有のカードで表されるため、同じツール統合に対して複数のカードが存在することがあります。 複数のパイプラインがある場合、各パイプラインはそれぞれ固有のカードで表されるため、同じツール統合に対して複数のカードが存在することがあります。 例えば、Microservices ツールチェーンを作成する場合、3 つのマイクロサービスのそれぞれが固有の GitHub リポジトリー、{{site.data.keyword.ghe_short}} リポジトリー、または Git リポジトリーと、固有のパイプラインを持ちます。
 {: tip}

## チュートリアルを始める: ツールチェーンの使用
{: #toolchain_tutorials}

[IBM&reg; Cloud Garage Method ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud/garage){:new_window} の以下のチュートリアルのいずれかをチェックアウトします。

  * [ 「Develop a Cloud Foundry app」ツールチェーンを使用した初めてのツールチェーンの作成と使用 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン ")](https://www.ibm.com/cloud/garage/tutorials/introduce-develop-cloud-foundry-app-toolchain){:new_window}。

  * [Add a toolchain to an app ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud/garage/tutorials/add-a-toolchain-to-an-app?task=2){:new_window}。

  * [Use the "Develop and test microservices on Cloud Foundry" toolchain ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud/garage/tutorials/use-develop-test-microservices-on-cloud-foundry-toolchain){:new_window}。
