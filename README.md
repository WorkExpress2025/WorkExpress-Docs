# WorkExpress-Docs







 





Documentação de um
Produto de Software

WorkExpress




Adan Marques
Adriano Lima
Danillo H. de Oliveira
Guilherme Oliveira Brandão da Silva
José Henrique Bronzatti Otero





              	







2024
ÍNDICE DETALHADO
1. Descrição do problema………………………………………………….. pg. 4
2. Proposta……………………………………………………………………. pg. 4
3. Cronograma……………………………………………………………….. pg. 4
4. Requisitos do sistema de software…………………………………… pg. 5
4.1 Requisitos funcionais………………………………………………….. pg. 5
4.2 Regras de negócio……………………………………………………… pg. 6
4.3 Requisitos não funcionas……………………………………………... pg. 7
4.4 Requisitos do processo……………………………………………….. pg. 8
5. Modelagem funcional……………………………………………………. pg. 9
5.1 Diagrama de caso de uso……………………………………………… pg. 9
5.2 Atores……………………………………………………………………… pg. 9
5.3 Especificação dos casos de uso……………………………………… pg. 10

1. Descrição do problema

No mercado já existem diversas plataformas de ofertas de serviços, elas são populares por terem amplo escopo de atuação, porém, apresentam alguns pontos falhos. Analisando o principal player do mercado, o GetNinjas, chegamos nos seguintes pontos:

1 – Por ser uma plataforma para todo tipo de oferta de serviço, tornou-se genérica, há poucas garantias de encontrar de fato, bons profissionais de determinados ramos;
2 – O modelo de negócio da plataforma prevê que a pessoa pague antes de conseguir um serviço, sendo pago valores altos apenas para enviar orçamentos aos clientes.

2. Proposta
Deste modo, a WorkExpress é uma plataforma que tem foco em construção civil, além disso, com um novo modelo de negócios que não prejudica o trabalhador pegando dinheiro dele antes de concluir um negócio.

3. Cronograma

Fase 1	Benchmarking e cerceamento do escopo	20/02/25 - 06/03/25
Fase 2	Análise técnica para implementação	27/02/25 - 13/03/25
Fase 3	Desenvolvimento	13/03/25 - 08/05/25
Fase 4	Testes e documentação	13/03/25 - 22/05/25
Fase 5	Apresentação	






















4.  Requisitos do Sistema de Software
4.1  Requisitos Funcionais

[RF001] – Cadastrar usuários na plataforma
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: Este requisito permite que o usuário se cadastre no site, os dados requeridos são: nome, e-mail, CPF, senha, idade e endereço completo.

[RF002] – Cadastrar prestador de serviço no site
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: Este requisito permite que o prestador de serviço se cadastre no site, os dados requeridos são: nome, e-mail, CPF, senha, idade e endereço completo.

[RF003] – Solicitar serviços	
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: Este requisito permite que o usuário solicite serviços.

[RF004] – Enviar orçamentos
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: Este requisito permite que o prestador de serviços envie orçamentos de seus custos.

[RF005] – Fechar negócio
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: Este requisito permite que o sistema ao identificar um aceite do usuário a um orçamento, registre que houve uma negociação bem-sucedida e feche o fluxo para recebimento de novos orçamentos.

[RF006] – Avaliar serviço
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: Este requisito permite que o usuário avalie o prestador.

[RF007] – Avaliar cliente
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: Este requisito permite o prestador avalie o usuário
4.2    Regras de Negócio

[RN001] – Cada pessoa pode ter apenas uma conta.
Descrição: Se uma pessoa fizer várias contas, ela pode burlar os sistemas de avaliação, a conta única é vinculada ao CPF.

[RN002] – Quanto maior a avaliação somada e mais serviços prestados ou solicitados, mais facilmente a pessoa estará nas listas de pesquisa
Descrição: Assim, tanto prestadores de serviço, quanto clientes, terão uma noção de quem são os mais confiáveis.

[RN003] – Pessoas constantemente mal avaliadas ou com reclamações recorrentes, correm o risco de serem bloqueadas
Descrição: As regras específicas serão criadas e apresentadas, porém, a expectativa é que pessoas enquadradas na descrição sejam bloqueadas em seus acessos.

[RN004] – Cada acordo de trabalho é bilateral e único.
Descrição: O cliente não pode fechar com vários prestadores diferentes para um mesmo serviço, a não ser que ele descreva ser um serviço para um grupo de pessoas, já se responsabilizando desde o começo, a pagar todos os envolvidos.

[RN005] – O tempo máximo para fechar um acordo é de duas semanas.
Descrição: Caso o cliente não aceite nenhuma proposta de serviço por mais de duas semanas, ela será excluída.

[RN006] – Criptografia das senhas
Descrição: A senha deve conter 8 caracteres, contendo um caractere maiúsculo, um digito e um caractere especial.
4.3   Requisitos Não-Funcionais

[RNF001] – Segurança
Prioridade:		Essencial	•	Importante		Desejável
Descrição: O sistema deve dispor de mecanismos de segurança para a autenticação de usuários e controle de acesso. A senha tem tamanho mínimo de 8 caracteres e só é aceita combinada ao e-mail. Além disso, sua recuperação se dá via e-mail do usuário.

[RNF002] – Usabilidade
Prioridade:		Essencial		Importante		Desejável
Descrição: O sistema deve prover interface de navegação de fácil aprendizagem de modo que gere a impressão de ser intuitiva. Visando criar uma experiência de uso positiva. Para tal, deve se basear em estudos de UX, sobretudo, sobre interfaces limpas e organizadas.

[RNF003] – Ajuda
Prioridade:		Essencial		Importante		Desejável
Descrição: O sistema deve prover aos usuários um manual de uso, para deixar claro seu objetivo e como a comunidade pode ajudar a torná-lo cada vez melhor. Esse manual ficará disposto em link no próprio aplicativo.

[RNF004] – Redundância
Prioridade:	•	Essencial		Importante		Desejável
Descrição: O sistema deve conter um robusto sistema de redundância para evitar que ele fique fora do ar, bem como seu banco de dados. Por exemplo, a máquina utilizada para ser seu servidor deve conter sistema anti-queda de energia e o banco de dados deve ter sistema de backups periódicos, em perídos de baixo acesso para evitar sobrecarregar o sistema.

[RNF005] – Pertencimento
Prioridade:		Essencial		Importante	•	Desejável
Descrição: O sistema deve conter meios de ampliar o senso de pertencimento e comunidade de seus usários, genrado assim uma comunidade que ativamente participe com sugestões do seu melhor desenvolvimento, em nível de experiência.

[RNF006] – Design
Prioridade:	•	Essencial		Importante		Desejável
Descrição: As técnicas de design, como tamanho do logo, jogo de cores, etc, devem ao mesmo tempo, auxiliar na usabilidade sendo esteticamente próxima aplicativos e sites conhecidos e bem avaliados, porém, com identidade visual única, que garanta que a marca seja reconhecida.

4.4 Requisitos de Processo

[RNF005] – Arquitetura de software
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: O sistema deve empregar arquitetura de (três) camadas: apresentação (React JS), algoritmo de backend (Spring) e dados (MySQL).

[RNF006] – Banco de Dados
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: O sistema deve utilizar o sistema gerenciador de banco de dados potente, compatível com múltiplas inserções e alterações.
[RNF007] – Hospedagem
Prioridade:		Essencial	•	Importante	•	Desejável
Descrição: O sistema deve ter seu servidor hospedado em nuvem, garantindo assim maior agilidade e segurança.

5. Modelagem Funcional
O sistema deve permitir que um usuário, previamente cadastrado, faça login e crie pedidos para serviços em construção civil.
Após criado, o serviço fica disponível para ser acessado por prestadores que enviarão orçamentos. Quando o usuário aceita um orçamento, um negócio é estabelecido e aquele serviço fica indisponível para outros prestadores.

	5.1 ATORES

Nome	Descrição
Usuário
	Usuário do sistema, previamente cadastrado, que irá solicitar serviços
Prestador de serviço	Pessoas capacitada que se canditará aos serviços

5.2 DIAGRAMA DE CASO DE USO



5.3  ESPECIFICAÇÃO DO CASO DE USO

CSU001 – Efetuar login
Sumário:	Este caso de uso tem como objetivo logar na plataforma.
Pré-condição:
O usuário ou prestador de serviço já ter realizado o cadastro no site
Fluxo Principal
Este caso de uso se inicia quando o ator usuário vai entrar no site
1. O ator usuário insere seu e-mail [RN1]
2. O ator usuário insere sua senha [RN6]
Fluxos Alternativos
[FA1] Fluxo Alternativo 1: Usuário não cadastrado
Este fluxo alternativo ocorre quando o usuário não tem conta cadastrada
 1.  O sistema exibe um campo de “Registro”
2.  O usuário se cadastra usando nome, e-mail, CPF, senha, idade e endereço completo.[RN1]

[FA1] Fluxo Alternativo 1: Esqueceu senha
Este fluxo alternativo ocorre quando o usuário esquece sua senha
1.	O sistema exibe um campo de esqueci senha
2.	usuário confirma o e-mail
3.	usuário recebe link para cadastrar nova senha [RN6]

Fluxos de Exceção
Este fluxo ocorre quando o ator usuário tenta cadastrar uma conta já existente
1. Após inserir os dados em Registro, se o sistema identifica que eles já correspondem a uma conta cadastrada, não segue com o cadastro.
2. Exibe mensagem, “Dados já pertencentes a uma conta cadastrada”

Pós-condições:
Não se aplica.
Regras de Negócio:
RN1, RN6

CSU002 – Criar solicitação
Sumário:	Este caso de uso tem como objetivo criar o a solicitação de serviço
Pré-condição:
Estar logado
Fluxo Principal
Este caso de uso se inicia quando o ator usuário já entrou no aplicativo
1. O ator usuário clica em criar solicitação
2. Abre tela de configuração
3. Solicitação criada com sucesso
Fluxos Alternativos
[FA1] Fluxo Alternativo

Fluxos de Exceção
Este fluxo ocorre se houver algum erro de criação:
1. O sistema exibe a mensagem: “Não é possível criar a solicitação neste momento, por favor, tente mais tarde”.
Pós-condições:
Não se aplica.
Regras de Negócio:


CSU003 – Configurar solicitação
Sumário:	Este caso de uso tem como objetivo configurar a solicitação.
Pré-condição:
Solicitação ter sido criada com sucesso.
Fluxo Principal
Este caso de uso se inicia quando o ator usuário já criou a solicitação
1. O ator usuário dá um nome à solicitação
2. Define data de início da solicitação.
3. Conclui a configuração.
4. Faz chamada ao Banco de Dados com as informações da solicitação criada.
Fluxos Alternativos
[FA1] Fluxo Alternativo

Fluxos de Exceção
1. O sistema exibe a mensagem: “Ocorreu um erro durante a configuração, por favor, tente novamente”
2. Caso o erro persista por três vezes seguidas, sistema exibe a mensagem: “Ocorreu um erro durante a configuração, por favor, tente mais tarde”
Pós-condições:
Não se aplica.
Regras de Negócio: RN5

CSU004 – Enviar orçamento
Sumário:	Este caso de uso tem como objetivo configurar a solicitação.
Pré-condição:
Solicitação estar configurada e disponível
Fluxo Principal
Este caso de uso se inicia quando o ator usuário já criou a solicitação
1. O ator prestador de serviço acessa à solicitação
2. Preenche os campos de orçamento
3. Conclui a clickando em “Enviar orçamento”.


CSU005 – Concluir negócio
Sumário:	Este caso de uso tem como objetivo concluir um negócio
Pré-condição:
Orçamento ter sido aceito pelo usuário.
Fluxo Principal
Este caso de uso se inicia quando o ator usuário já aceitou o orçamento
1. O ator usuário clica em “Fechar negócio”
2. O ator prestador de serviço recebe uma mensagem e e-mail
Fluxos Alternativos
[FA1] Fluxo Alternativo

Fluxos de Exceção
1. O sistema exibe a mensagem: “Ocorreu um erro, por favor, tente novamente”
2. Caso o erro persista por três vezes seguidas, sistema exibe a mensagem: “Ocorreu um erro, vamos enviar um e-mail avisando o desejo de finalizar o negócio para XXXX, por favor, confirme novamente mais tarde”
Pós-condições:
Não se aplica.
Regras de Negócio: RN4


