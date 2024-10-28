# Resumo-lab-3-dio

## Passo a passo para configurar uma instância do Azure SQL Database

### 1. Acessar o Portal da Azure

Entre no Portal da Azure e faça login com sua conta.


### 2. Navegar até "Banco de Dados SQL"

No menu à esquerda, clique em "Banco de Dados SQL" ou pesquise por "Banco de Dados SQL" na barra de pesquisa no topo.


### 3. Criar um Novo Banco de Dados

Na página de bancos de dados SQL, clique em "Criar" e selecione "Banco de Dados SQL".


### 4. Configurar as Informações Básicas

Preencha os detalhes básicos do banco de dados:

Assinatura: Selecione a assinatura da Azure que você está utilizando.

Grupo de Recursos: Selecione um grupo de recursos existente ou crie um novo.

Nome do Banco de Dados: Escolha o nome para seu banco de dados (ex: "BancoFinanceiro").

Servidor: Você precisará criar um servidor ou selecionar um servidor existente:

Criar Servidor: Ao clicar para criar um novo servidor, preencha os campos:

Nome do servidor (único, ex: "servidor-financeiro").

Região (escolha a mesma região do banco de dados).

Nome de login e senha do administrador do servidor. Essas credenciais serão usadas para gerenciar o banco.



Modo de Compra: Escolha o plano de pagamento baseado no desempenho necessário:

VCore: Selecione o número de núcleos virtuais (vCores), o que afeta o desempenho e o custo.

Serviço Gerenciado: Para bancos de dados menores ou em modo simples, você pode selecionar o nível Básico ou Standard.



### 5. Escolher o Nível de Serviço

Escolha o nível de serviço de acordo com as necessidades de desempenho e armazenamento do seu banco de dados:

Uso Geral: Para cargas de trabalho regulares, com bom equilíbrio entre custo e desempenho.

Negócios Críticos: Para bancos que precisam de alta disponibilidade e maior resiliência.

Hyperscale: Para bancos de dados muito grandes com necessidade de escalabilidade rápida.


Você também pode definir o tamanho do banco de dados e os requisitos de backup.

### 6. Configurar as Redes

Configure o acesso de rede ao banco de dados:

Escolha se deseja permitir o acesso do banco de dados somente de redes privadas ou de redes públicas.

Configure o firewall. Permita acessos específicos inserindo endereços IP confiáveis, como seu IP local, para conectar-se ao banco via ferramentas de administração (SSMS, por exemplo).



### 7. Configurações Adicionais (opcional)

Backup e Redundância: Defina políticas de backup para retenção de dados e estratégias de recuperação de desastres (backup local, georreplicação, etc.).

Segurança: Configure a autenticação adicional, como Autenticação do Azure Active Directory (AAD), que permite usar o Azure AD para gerenciar permissões e acesso ao banco de dados.

Monitoramento: Ative a Auditoria e Diagnóstico para acompanhar a integridade do banco de dados e acessar logs detalhados.


### 8. Revisar e Criar

Revise todas as configurações na seção "Revisar + Criar". O Azure fará uma verificação para garantir que as configurações estão corretas.

Clique em "Criar".


### 9. Aguardar a Implantação

O Azure criará e configurará o banco de dados. O processo de criação da instância pode levar alguns minutos.

Após a criação, você verá uma mensagem de sucesso e poderá acessar o banco de dados.


### 10. Conectar ao Banco de Dados

Para gerenciar e acessar seu banco de dados, você pode usar ferramentas como o SQL Server Management Studio (SSMS) ou ferramentas de linha de comando, como o Azure CLI ou SQLCMD.

Ao se conectar, use as credenciais do administrador configuradas na etapa de criação do servidor e o nome do servidor no formato:

servidor-financeiro.database.windows.net

Porta: O banco de dados SQL da Azure usa a porta 1433.


### 11. Gerenciar e Monitorar o Banco de Dados

No portal da Azure, você pode acessar o painel do banco de dados para monitorar o desempenho, ajustar as configurações, e executar consultas SQL diretamente no portal.

O banco de dados pode ser integrado com outras soluções de monitoramento da Azure, como o Azure Monitor, para configurar alertas e relatórios automáticos sobre desempenho e utilização dos recursos.
