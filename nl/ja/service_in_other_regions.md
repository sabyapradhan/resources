---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-26"

keywords: service availability, service location, using services across regions

subcollection: resources

---

{:shortdesc: .shortdesc}

# 他の地域でサービスを利用する
{: #cross_region_service}

ある地域でサービス・インスタンスを作成してアプリにバインドした場合、以下のいずれかの方法でそのサービス・インスタンスを他の地域で利用できます。
{: shortdesc}

  * サービス資格情報を使用して、アプリ・インスタンスを直接構成します。 詳しくは、『[外部アプリへのサービスの接続](/docs/resources?topic=resources-externalapp#externalapp)』を参照してください。
  * ブリッジとしてユーザー提供サービスを作成します。

	他の地域にあるサービス・インスタンスを利用するには、以下のステップを実行します。

      1. サービス・インスタンスが存在する地域に切り替えるには、**「メニュー」アイコン ![「メニュー」アイコン](../icons/icon_hamburger.svg)**>**「リソース・リスト」**をクリックします。 次に、**「ロケーション」**メニューを展開し、地域を選択します。

      2. サービスの存在する地域にあるサービス・インスタンスの VCAP_SERVICES 環境変数から、資格情報と接続パラメーターを取り出します。 以下のステップを実行します。

	       1. {{site.data.keyword.Bluemix_notm}} ダッシュボードで、アプリ・タイルの**「すべて表示」**をクリックします。 「概要」ページが表示されます。
	       2. ナビゲーション・ペインで、**「資格情報」**をクリックします。 *VCAP_SERVICES* 環境変数の詳細が表示されます。 サービス・インスタンスの JSON コンテンツを記録します。

      3. サービス・インスタンスを利用する地域に切り替えます。 **「メニュー」アイコン ![「メニュー」アイコン](../icons/icon_hamburger.svg)**>**「リソース・リスト」**をクリックします。 次に、**「ロケーション」**メニューを展開し、サービス・インスタンスを使用する地域を選択します。

      4. *VCAP_SERVICES* 環境変数から記録した資格情報と接続パラメーターを使用して、ユーザー提供のサービス・インスタンスを作成します。 詳しくは、[ユーザー提供のサービス・インスタンスの作成](/docs/apps/tutorials?topic=creating-apps-add-resource#user_provide_services)を参照してください。

      5. 以下のコマンドを使用して、ユーザー提供のサービス・インスタンスをアプリにバインドします。

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
