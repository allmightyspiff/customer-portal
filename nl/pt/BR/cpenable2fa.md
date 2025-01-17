---

copyright:

  years: 2018, 2019

lastupdated: "2019-04-25"

keywords: PhoneFactor authentication, two-factor authentication, PIN type, 2FA 

subcollection: customer-portal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Configurando a autenticação de dois fatores
{: #cp_setup-2fa}

No portal do cliente, a autenticação externa de dois fatores (2FA) poderá ser ativada para incluir proteção extra quando você efetuar login no portal. Essa camada extra de segurança protege a conta contra acesso não verificado, assegurando que dispositivos, dados e informações de conta sejam protegidos.
{:shortdesc}

Se você ativar a 2FA no portal do cliente de sua conta existente do SoftLayer, será necessário inserir seu código de segurança quando efetuar login no console do {{site.data.keyword.Bluemix_notm}}. A 2FA aplica-se somente aos recursos de infraestrutura em sua conta do {{site.data.keyword.Bluemix_notm}}. É possível executar várias ações para os recursos em sua conta do {{site.data.keyword.Bluemix_notm}} sem concluir a 2FA.

A 2FA para a sua conta do SoftLayer não é por IBMid. Ainda é por conta. Quando um IBMid está associado a múltiplas contas e você alterna entre as contas, deve-se confirmar sua identidade toda vez que alterna para uma conta diferente. Deve-se confirmar sua identidade quando você alterna entre contas mesmo se a conta anterior e a nova conta são configuradas com o mesmo mecanismo 2FA.

## Ativando a 2FA
{: #cp-enable-2fa}

A autenticação 2FA está disponível em duas formas. Ambos os métodos de autenticação externa podem ser incluídos para cada usuário por uma pequena taxa mensal:

* O Symantec Identify Protection é a ferramenta de autenticação externa mais comumente usada, que fornece um código de segurança dinâmico usado além do nome de usuário e da senha ao acessar o Portal do cliente.
* A autenticação PhoneFactor fornece autenticação fora da banda com um telefonema, SMS ou aplicativo móvel.

 Se você tiver uma conta vinculada, será possível aproveitar a configuração da autenticação de diversos fatores (MFA) [ativando a autenticação de diversos fatores](/docs/iam?topic=iam-enablemfa#enablemfa) para toda a sua conta do {{site.data.keyword.Bluemix_notm}}.
 {: tip}

Para configurar a 2FA, conclua as etapas a seguir:

1. Acesse **Conta** > **Usuários** e, em seguida, clique em **Lista de usuários**.
2. Selecione **Incluir autenticação externa** no menu **Ações** para o usuário.
3. Com base no tipo de autenticação externa que está sendo solicitada, conclua as etapas a seguir:
    * Se você escolher Symantec Identity Protection, selecione **Symantec Identity Protection** e, em seguida, insira o ID da credencial do usuário.
    * Se você escolher PhoneFactor, selecione **PhoneFactor**.
4. Clique em **Continuar**.
5. Conclua os prompts na tela para o **Código promocional** e **Confirmação de MSA**.
6. Clique em **Autenticação externa do pedido** para concluir o pedido. Clique em **Cancelar** para cancelar a ação.

## Próximas Etapas
{: #2fanextsteps}

Depois de incluir a autenticação externa para um usuário, as próximas etapas dependem do tipo de autenticação.
* Se o Symantec Identity Protection está ativado, deve-se incluir o código de segurança associado ao ID da credencial do usuário. Esse código de segurança é aquele que foi inserido no sistema no momento em que o Symantec Identity Protection foi incluído na conta.
* Se o PhoneFactor está ativado, o usuário deve ativar o PhoneFactor para usar esse tipo de autenticação de dois fatores com a conta.

### Ativando a autenticação do PhoneFactor
{: #cp_phonefacauth}

Depois de incluir o PhoneFactor, deve-se ativar manualmente a autenticação externa com o PhoneFactor por meio do portal do cliente. Como o PhoneFactor usa contato manual, é importante assegurar que todos os números de telefone associados à conta estejam sempre atualizados. A falha em manter as informações de contato atualizadas poderá resultar na impossibilidade de acessar o portal do cliente e a VPN quando o PhoneFactor estiver ativo. Quando o PhoneFactor for incluído com êxito, você receberá um e-mail para confirmar que o PhoneFactor foi incluído. Depois de receber o e-mail, use as etapas a seguir para ativar a autenticação do PhoneFactor.

1. Acesse o portal do cliente usando as suas credenciais exclusivas.
2. Selecione **Conta > Usuários** na barra de navegação.
3. Clique no nome do usuário para acessar o perfil do usuário associado para ele.
4. Role para a seção **Configurações do PhoneFactor**.

  Se a seção Configurações do PhoneFactor não estiver disponível, verifique primeiro se você recebeu o e-mail de fornecimento do PhoneFactor, o que indica que ele foi provisionado. Se o PhoneFactor for provisionado e a seção não estiver disponível, crie um chamado de suporte. Se o PhoneFactor ainda não tiver sido provisionado, aguarde o e-mail e tente novamente.
  {: tip}

5. Selecione **Ativo** na lista **Status**.
6. Edite o **Número do telefone principal** para autenticação.
  1. Clique no link **Editar**.
  2. Insira o **Código do país**, o **Número do telefone** e o **Ramal**, se aplicável, nos campos associados.
  3. Clique em **Autenticar e salvar número** para concluir a autenticação.

    Quando você inclui um número de telefone para autenticação, deve-se estar no telefone. Depois de clicar em **Autenticar**, o número é chamado e é solicitado que você conclua uma etapa para autenticar o número. Os números de telefone não podem ser autenticados sem a conclusão dessas etapas.
    {: tip}

  4. Para incluir um **Número de telefone secundário**, repita essas etapas.
7. Selecione o **Método de contato** na lista **Método**.
8. Selecione um **Tipo de PIN** na lista **Tipo de PIN**.
9. Se você selecionar **Uma Vez** > **Valor de PIN**, insira o PIN no campo **Valor do PIN**.
10. Clique em **Atualizar** para atualizar as mudanças e ativar a autenticação do PhoneFactor.

Depois de ativar o PhoneFactor, a autenticação por meio dele é necessária para o portal do cliente ou a VPN. Após a autenticação com as credenciais do usuário, uma mensagem informa que a autenticação do PhoneFactor está sendo tentada. Você, ou o usuário que está sendo incluído, deve estar perto do telefone listado com o PhoneFactor para concluir a autenticação. O PhoneFactor tenta autenticar cinco vezes. Após cinco tentativas de autenticação malsucedidas, você fica bloqueado por aproximadamente uma hora. Você, ou um usuário com acesso administrativo à conta, pode mudar as configurações de autenticação do PhoneFactor a qualquer momento. Você, ou um administrador da conta, pode desativar o PhoneFactor a qualquer momento.

 Se você optar por configurar o PhoneFactor para o portal do cliente e seu login da VPN, o resultado serão dois processos separados de login 2FA, um para o portal do cliente e outro para a VPN.
 {: tip}

#### Métodos de autenticação do PhoneFactor
{: #cp_authmeths}

Se você configura o PhoneFactor como o tipo de autenticação, é possível escolher uma das opções a seguir como um método de autenticação:

<dl>
<dt>Telefonema e padrão (sem PIN)</dt>
<dd>Com essa opção ativada, ao efetuar login no portal, você recebe um telefonema no número primário ativado. Ao responder a chamada, é pedido que você pressione a tecla # para concluir a autenticação.</dd>
<dt>Telefonema com PIN</dt>
<dd>Com essa opção selecionada, você insere um valor de PIN no portal do cliente. O PIN deve ter de 4 a 8 números. Ao tentar efetuar login no portal, você recebe uma chamada para o número primário listado no portal. Ao responder, é pedido que você deve insira o número do PIN seguido pelo # para concluir a autenticação.</dd>
<dt>Texto SMS e PIN único</dt>
<dd>Com essa opção selecionada, você recebe uma mensagem de texto com um PIN que será usado para responder à mensagem. Quando você insere o PIN fornecido, o processo de autenticação é concluído e efetua seu login no portal.</dd>
<dt>Texto SMS com valor de PIN único</dt>
<dd>Com essa opção selecionada, você cria um valor de PIN de 4 a 8 números. Em seguida, você recebe uma mensagem de texto e responde com o código fornecido e o número do PIN sem espaços.</dd>
<dt>Aplicativo PhoneFactor e padrão (sem PIN)</dt>
<dd>Abra o aplicativo PhoneFactor (Microsoft Autenticator) em seu dispositivo e clique em <strong>Autenticar</strong>. Ele mostra que você foi autenticado com êxito usando o PhoneFactor e efetua seu login no portal.</dd>
<dt>Aplicativo PhoneFactor com PIN</dt>
<dd>Com essa opção, você configura um PIN de 4 a 8 números no portal. Em seguida, você abre o aplicativo PhoneFactor (Microsoft Autenticator) em seu dispositivo. Em seguida, insira seu PIN que foi criado no portal e clique em <strong>Autenticar</strong> para efetuar login no portal.</dd>
</dl>
