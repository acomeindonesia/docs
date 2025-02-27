---
title: Habilitando a sincronização automática de licença de usuário para sua empresa
intro: 'Você pode gerenciar o uso da licença entre os seus ambientes de {% data variables.product.prodname_enterprise %} sincronizando automaticamente as licenças de usuário de {% data variables.product.product_location %} com {% data variables.product.prodname_ghe_cloud %}.'
redirect_from:
  - /enterprise/admin/installation/enabling-automatic-user-license-sync-between-github-enterprise-server-and-github-enterprise-cloud
  - /enterprise/admin/configuration/enabling-automatic-user-license-sync-between-github-enterprise-server-and-github-enterprise-cloud
  - /admin/configuration/enabling-automatic-user-license-sync-between-github-enterprise-server-and-github-enterprise-cloud
  - /admin/configuration/managing-connections-between-github-enterprise-server-and-github-enterprise-cloud/enabling-automatic-user-license-sync-between-github-enterprise-server-and-github-enterprise-cloud
  - /admin/configuration/managing-connections-between-your-enterprise-accounts/enabling-automatic-user-license-sync-between-github-enterprise-server-and-github-enterprise-cloud
permissions: Enterprise owners can enable automatic user license synchronization.
versions:
  ghes: '*'
type: how_to
topics:
  - Enterprise
  - GitHub Connect
  - Licensing
shortTitle: Sincronização automática da licença do usuário
---

## Sobre a sincronização de licenças

{% data reusables.enterprise-licensing.about-license-sync %} Para obter mais informações, consulte "[Sobre {% data variables.product.prodname_github_connect %}de](/admin/configuration/configuring-github-connect/about-github-connect#data-transmission-for-github-connect)."

If you enable automatic user license sync for your enterprise, {% data variables.product.prodname_github_connect %} will automatically synchronize license usage between {% data variables.product.prodname_ghe_server %} and {% data variables.product.prodname_ghe_cloud %} weekly.{% ifversion ghes > 3.4 %} You can also synchronize your license data at any time outside of the automatic weekly sync, by manually triggering a license sync job. For more information, see "[Triggering a license sync job](/billing/managing-your-license-for-github-enterprise/syncing-license-usage-between-github-enterprise-server-and-github-enterprise-cloud#triggering-a-license-sync-job)."{% endif %}

Se você usar várias instâncias de {% data variables.product.prodname_ghe_server %}, você pode habilitar a sincronização automática de licença entre cada uma de suas instâncias e a mesma organização ou conta corporativa em {% data variables.product.prodname_ghe_cloud %}.

{% data reusables.enterprise-licensing.view-consumed-licenses %}

Você também pode fazer upload manualmente das informações de licença do usuário do {% data variables.product.prodname_ghe_server %} para o {% data variables.product.prodname_ghe_cloud %}. Para obter mais informações, consulte "[Sincronizando uso de licença entre {% data variables.product.prodname_ghe_server %} e {% data variables.product.prodname_ghe_cloud %}](/billing/managing-your-license-for-github-enterprise/syncing-license-usage-between-github-enterprise-server-and-github-enterprise-cloud)".

{% data reusables.enterprise-licensing.verified-domains-license-sync %}

## Habilitar a sincronização de licenças

Antes de habilitar a sincronização de licença em {% data variables.product.product_location %}, você deverá habilitar {% data variables.product.prodname_github_connect %}. Para obter mais informações, consulte "[Gerenciando {% data variables.product.prodname_github_connect %}](/admin/configuration/configuring-github-connect/managing-github-connect)".

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.github-connect-tab %}
1. Em "Server can sync user license count and usage" (Servidor pode sincronizar contagem e uso de licenças de usuário), selecione **Enabled** (Habilitado) no menu suspenso. ![Menu suspenso para habilitar a sincronização automática de licenças de usuário](/assets/images/enterprise/site-admin-settings/enable-user-license-drop-down.png)
