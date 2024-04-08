# Sistema de Gestão Hospitalar
Sistema de Gestão Hospitalar utilizando MySQL, PHP e Bootstrap

## Precisa trabalhar em:

1. Capacidade de aceitar a consulta do médico para reconhecer ao paciente que sua consulta foi aprovada.
2. O usuário não deverá ser autorizado a se registrar se tentar fornecer o ID de e-mail já registrado.
3. A senha deve ser criptografada e o campo de senha não deve ser exibido no painel de administração.
4. Implementação de paginação para todas as visualizações de lista do aplicativo.
5. Correção de bug - O recibo de pagamento da conta contém vários registros se o paciente tiver se associado ao mesmo médico várias vezes.
6. Adição de mais campos na declaração de prescrição para torná-la mais específica.
7. Adição de mais detalhes sobre o pagamento - como data do pagamento efetuado, valor pago, etc.
8. Implementação do botão de exportação no módulo de administração para exportar todos os detalhes para uma planilha Excel.

## Pré-requisitos
1. Instale o servidor web XAMPP
2. Qualquer editor (de preferência VS Code ou Sublime Text)
3. Qualquer navegador com versão mais recente

## Idiomas e tecnologias utilizadas
1.HTML5/CSS3
2. JavaScript (para criar conteúdo de atualização dinâmica)
3. Bootstrap (uma biblioteca HTML, CSS e JS)
4. XAMPP (um servidor web da Apache Friends)
5. PHP
6. MySQL (um RDBMS que usa SQL)
7. TCPDF (para gerar PDFs)

## Passos para executar o projeto em sua máquina
1. Baixe e instale o XAMPP em sua máquina
2. Clone ou baixe o repositório
3. Extraia todos os arquivos e mova-os para a pasta ‘htdocs’ do seu diretório XAMPP.
4. Inicie o Apache e o Mysql no painel de controle do XAMPP.
5. Abra seu navegador e digite ‘localhost/phpmyadmin’
6. Na página phpmyadmin, crie um novo banco de dados no painel esquerdo e nomeie-o como ‘myhmsdb’
7. Importe o arquivo 'myhmsdb.sql' dentro do seu banco de dados recém-criado e clique em ok.
8. Abra uma nova aba e digite ‘localhost/foldername’ na URL do seu navegador
9. Viva! É isso!
    
### SOFTWARES USADOS
  - O XAMPP foi instalado na máquina Ubuntu 19.04 e o Servidor APACHE2 e MySQL foram inicializados. E os arquivos foram criados dentro de opt/lampp/htdocs/myhmsp
  - Sublime Text 3.2 foi usado como editor de texto.
  - Google Chrome versão 77.0.3865.90 foi usado para executar o projeto (localhost/myhmsp foi usado como url).
  

### Iniciando Apache e MySQL no XAMPP:
  O Painel de Controle do XAMPP permite iniciar e parar manualmente o Apache e o MySQL. Para iniciar o Apache ou MySQL manualmente, clique no botão ‘Iniciar’ em ‘Ações’.
  
  
<p align="center"><img src="https://user-images.githubusercontent.com/36665975/59350977-fcc68900-8d3a-11e9-9450-e5c478497caa.png"></img></p>

## ENTRAR NO PROJETO:
Sistema de Gestão Hospitalar em php e mysql. Este sistema possui uma página inicial onde o paciente, médico e administrador podem fazer login em suas contas alternando as guias de acordo. A Fig 1.1 mostra a página ‘Home’ do nosso projeto.

![imagem](https://user-images.githubusercontent.com/36665975/66569676-ad2d8800-eb89-11e9-94e5-ea407622a1fe.png)

A página 'Sobre nós' (Fig 1.2) permite-nos obter mais informações sobre a qualidade e os serviços do hospital.

![imagem](https://user-images.githubusercontent.com/36665975/66569816-f4b41400-eb89-11e9-9377-d9ce53ded088.png)

A página ‘Contato’ permite que os usuários forneçam comentários ou dúvidas sobre os serviços do hospital. A Fig 1.3 mostra a página ‘Contato’.

![imagem](https://user-images.githubusercontent.com/36665975/66569890-157c6980-eb8a-11e9-9b2f-c0e8a6ef702e.png)

A página ‘Home’ consiste em 3 módulos:
1. Módulo Paciente
2. Módulo Médico
3. Módulo de administração

### Módulo Paciente:

  &nbsp; &nbsp; &nbsp; Este módulo permite que os pacientes criem sua conta, marquem uma consulta médica e vejam seu histórico de consultas.
  A página de registro (na própria página inicial) pede aos pacientes que insiram seu nome, sobrenome, ID de e-mail, número de contato, senha e botões de opção para selecionar seu sexo.
  
  ![imagem](https://user-images.githubusercontent.com/36665975/66570027-5b393200-eb8a-11e9-9e97-088630b5e583.png)

Assim que o paciente tiver criado sua própria conta após clicar no botão ‘Cadastre-se’, ele será redirecionado para seu Painel (Fig. 1.5).

![imagem](https://user-images.githubusercontent.com/36665975/66570123-8c196700-eb8a-11e9-845f-ea02013f1d5c.png)

A página Painel permite que os pacientes realizem duas operações:

**1. Marque sua consulta:**

  &nbsp; &nbsp; &nbsp; Aqui, os pacientes podem marcar consultas médicas. O formulário de consulta (Fig. 1.6) exige que os pacientes selecionem o médico que desejam consultar, a data e a hora em que desejam se encontrar com o médico. O valor da consultoria será mostrado de acordo com o paciente, pois já foi determinado pelo médico.

![imagem](https://user-images.githubusercontent.com/36665975/66570202-c256e680-eb8a-11e9-8839-6c7fef68ac4c.png)

Após clicar no botão ‘Criar nova entrada’, o paciente receberá um alerta que confirma o sucesso da consulta do paciente. (Ver Fig 1.7)

![imagem](https://user-images.githubusercontent.com/36665975/66570280-ec100d80-eb8a-11e9-96c2-08e5441954d0.png)

**2. Ver histórico de consultas dos pacientes:**

  &nbsp; &nbsp; &nbsp; Aqui, o paciente pode ver seu histórico de consultas que contém nome do médico, taxa de consulta, data e hora da consulta (ver Fig 1.8).

![imagem](https://user-images.githubusercontent.com/36665975/66570349-0ea22680-eb8b-11e9-94fe-22a86070a274.png)

Depois que o paciente tiver saído de sua conta, se quiser entrar novamente em sua conta, ele poderá fazer login em sua conta, em vez de registrá-la novamente. A Fig 1.9 mostra a página de login.
Clicar no botão ‘Login’ redirecionará o paciente para a página do painel que vimos anteriormente (Fig 1.5)

![imagem](https://user-images.githubusercontent.com/36665975/66570502-588b0c80-eb8b-11e9-88e3-5294ae896ace.png)

É assim que funciona o módulo do paciente. No geral, este módulo permite ao paciente cadastrar sua conta ou fazer login na sua conta (se tiver), marcar uma consulta e visualizar seu histórico de consultas.

### Módulo Médico:

  &nbsp; &nbsp; &nbsp; Os médicos podem fazer login em sua conta, o que pode ser feito alternando a guia de ‘Paciente’ para ‘Médico’. A Fig 1.10 mostra o formulário de login de um médico. O registro de uma conta médica só pode ser feito pelo administrador. Discutiremos mais sobre isso no Módulo Admin.
  
![imagem](https://user-images.githubusercontent.com/36665975/66570609-8bcd9b80-eb8b-11e9-8099-9f285aa7fe0f.png)

Assim que o médico clicar no botão ‘Login’, ele será redirecionado para seu próprio painel, mostrado na Figura 1.11

![imagem](https://user-images.githubusercontent.com/36665975/66570642-a0119880-eb8b-11e9-8d23-be898e1bfa29.png)

Nesta página o médico poderá ver as consultas agendadas pelos pacientes. A Fig 1.12 mostra a consulta do médico ‘Ganesh’ que foi marcada pelo paciente ‘Kenny Sebastian’ (Fig 1.6). Isso significa que o médico ‘Ganesh’ terá uma consulta com o paciente ‘Kenny Sebastian’ no dia 10/10/2019 às 10h.

![imagem](https://user-images.githubusercontent.com/36665975/66570704-be779400-eb8b-11e9-92ae-21d8e0e4aba4.png)

Em tempo real, os médicos terão milhares de consultas. Será mais fácil para o médico procurar consulta no caso de mais consultas. Para facilitar, tenho uma caixa de ‘Pesquisa’ na barra de navegação (ver Fig 1.12) que permite aos médicos procurar um paciente pelo seu número de contacto.
&nbsp; &nbsp; &nbsp; Depois que tudo estiver feito, o médico poderá sair da sua conta. Assim, em geral, um médico pode acessar sua conta, visualizar suas consultas e procurar um paciente. Isso é tudo sobre o Módulo Doutor.

### Módulo de administração:
   
   &nbsp; &nbsp; &nbsp; Este módulo é o coração do nosso projeto, onde um administrador pode ver a lista de todos os pacientes. Médicos e consultas e comentários/dúvidas recebidos na página ‘Contato’. Além disso, o administrador também pode adicionar médico.
  &nbsp; &nbsp; &nbsp; O login na conta de administrador pode ser feito alternando para a guia admin da página inicial. A Fig 1.13 mostra a página de login do administrador.
  &nbsp; &nbsp; &nbsp; `nome de usuário`: admin, `senha`: admin123

![imagem](https://user-images.githubusercontent.com/36665975/66570795-e961e800-eb8b-11e9-94e2-79940ff1d45e.png)

Ao clicar no botão ‘Login’, o administrador será redirecionado para seu painel conforme mostrado em
Figura 1.14.

![imagem](https://user-images.githubusercontent.com/36665975/66570841-03032f80-eb8c-11e9-9cfc-62b6b869c918.png)

Este módulo permite que o administrador execute cinco operações principais:
**1. Veja a lista de todos os pacientes cadastrados:**

  &nbsp; &nbsp; &nbsp; O administrador pode visualizar todos os pacientes cadastrados. Isso inclui o nome, sobrenome, ID de e-mail, número de contato e senha dos pacientes. (Ver Fig 1.15). Assim como no módulo médico, o administrador também pode procurar um paciente pelo número de contato na caixa de pesquisa.
  
  ![imagem](https://user-images.githubusercontent.com/36665975/66571179-83c22b80-eb8c-11e9-8819-008cdd2b0c2e.png)
  
**2. Veja a lista de todos os médicos cadastrados:**

  &nbsp; &nbsp; &nbsp; Detalhes dos médicos também podem ser visualizados pelo administrador. Esses detalhes incluem o nome do médico, senha, e-mail e honorários de consultoria, mostrados na Figura 1.16. A procura de um médico pode ser feita usando o ID de e-mail do médico na caixa de pesquisa.

![imagem](https://user-images.githubusercontent.com/36665975/66571329-a5bbae00-eb8c-11e9-89be-ce1a9c73e01b.png)

**3. Veja as listas de compromissos:**

  &nbsp; &nbsp; &nbsp; O administrador também pode ver todos os detalhes da consulta que mostra os detalhes da consulta dos pacientes com seus respectivos médicos. Isso inclui nome, sobrenome, e-mail e número de contato dos pacientes, nome do médico, data da consulta, horário e honorários da consultoria. (Ver Figura 1.17).
  
  ![imagem](https://user-images.githubusercontent.com/36665975/66571377-c3891300-eb8c-11e9-92d2-6755204564c7.png)
  
**4. Adicionar médico:**

  &nbsp; &nbsp; &nbsp; Somente o administrador pode adicionar um novo médico, já que qualquer pessoa pode se registrar como médico se colocarmos esta seção na página inicial. Este formulário solicita o nome do médico, ID de e-mail, senha e honorários de consultoria. (Ver Fig 1.18)
  
  ![imagem](https://user-images.githubusercontent.com/36665975/66571687-55911b80-eb8d-11e9-9859-54e15d4ad8a0.png)
  
  Após adicionar um novo médico, se verificarmos a lista do médico, veremos os detalhes do novo médico adicionado à lista conforme mostrado na Figura 1.19
  
  ![imagem](https://user-images.githubusercontent.com/36665975/66571496-03e89100-eb8d-11e9-954e-7e3704bd0ca3.png)
  
**5. Ver comentários/consultas do usuário:**

  &nbsp; &nbsp; &nbsp; O administrador tem permissão para visualizar o feedback/consulta fornecido pelo usuário na página ‘Contato’ (consulte a Figura 1.3). Isso inclui o nome do usuário, ID de e-mail, número de contato e a mensagem (Feedback/Consulta), conforme mostrado na Figura 1.20.
  
  ![imagem](https://user-images.githubusercontent.com/36665975/66571573-27134080-eb8d-11e9-8c1f-191a9f491872.png)
  
  &nbsp; &nbsp; &nbsp; Levando tudo em consideração, o administrador pode visualizar os dados dos pacientes e médicos, detalhes da consulta, feedback do usuário e adicionar um novo médico. Depois que tudo estiver feito, o administrador poderá sair de sua conta.

## Atualizações

### 1. Cancelar compromissos

   &nbsp; &nbsp; &nbsp; Pacientes e médicos podem excluir suas consultas.
 
   ![imagem](https://user-images.githubusercontent.com/36665975/75169587-d0c72880-574e-11ea-9a9e-ba098c04e594.png)
    
  Se o paciente excluir o último registro (para o médico Ganesh), um rótulo "excluído por você" será exibido na coluna 'Status Atual' e a ação mudará para o estado de cancelamento.
  
  ![imagem](https://user-images.githubusercontent.com/36665975/75169873-47642600-574f-11ea-8ca4-420b0dfd20c3.png)
  
  Agora, se acessarmos a conta do médico Ganesh e visualizarmos os detalhes de sua consulta, ficará assim:
  
  ![imagem](https://user-images.githubusercontent.com/36665975/75170076-9316cf80-574f-11ea-84ff-6a5976ce8179.png)
  
  Da mesma forma, os médicos também podem excluir suas consultas e os pacientes podem visualizar os detalhes atualizados das consultas.
  
### 2. Remover médicos por administrador

&nbsp; &nbsp; &nbsp; O administrador também pode excluir os médicos do sistema. Isso permite que o administrador tenha mais controle sobre o sistema.

![imagem](https://user-images.githubusercontent.com/36665975/75170650-6d3dfa80-5750-11ea-8f05-455c7d704217.png)
  




