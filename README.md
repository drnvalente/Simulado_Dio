# Simulado Dio
Repositório destinado para avalição de desafio da Dio no curso Santander Cibersegurança 2025
# Principais tipos de ataques

Entendendo os tipos de ataques que são descritos no curso, são divididos em Ataque de Dicionário, Ataque de Força Bruta Pura (Permutação) e Ataque Híbrido que utiliza Mangling Rules e Junção de Listas.
1- Ataque de Dicionário: trabalha utilizando arquivos de textos contendo uma série de senhas já utilizadas por seres humanos, são comumente encontradas na internet, utilizando um software que vai testar as senhas que estão contidas nas listas;
2- Ataque de Força Bruta Pura (Permutação): Ataque que é executado com software que gera as possíveis combinações de senhas possíveis, considerado inviável pois demanda tempo e é inútil para ambientes que utilizam MFA.
3- Ataque Híbrido:
  3.1 Mangling Rules: Consiste basicamente em substituir as letras por caracteres, levando em consideração os padrões de criação de senhas por seres humanos.
  3.2 Junção de Listas: Utiliza duas ou mais listas para testar as combinações, tem melhor desempenho se  atacante já tiver coletados dados dos usuários previamente.
  
# Password Sprayng e Credential Stuffing
  1.1 Password Sprayng: Consiste em testar senhas fracas em todos os usuários de e-mail de uma corporação que esta sendo atacada, afim de identificar o uso da mesma senha para vários usuários.
  1.2 Credential Stuffing: Consiste em levantar dados vazados e por tentativa testar senhas que o usuário utiliza em outros locais como sites e-mails etc, para tntar acessar outras contas do mesmo usuário que utilizam a mesma senha em vários ambientes.
  
# Ferramentas de ataque:
1- Sistema Operacional Kali Linux: Consiste em uma distribuição Linux votada para testes de penetração pois já vem com todas as ferramentas necessárias.
2- Medusa: Ela é usada principalmente para realizar ataques de força bruta e ataques de dicionário em serviços de rede, buscando descobrir credenciais de acesso válidas (nomes de usuário e senhas).
3- Hydra: Assim como o Medusa, seu principal objetivo é descobrir credenciais de login válidas explorando a fragilidade das senhas em diversos serviços de rede.
4- Ncrack: Embora o Ncrack realize a mesma função básica de força bruta que o Hydra e o Medusa, ele se destaca por alguns pontos importantes:
  4.1 Foco na Confiabilidade: Ele foi projetado para ser confiável em larga escala, o que é crucial ao testar grandes redes com muitos hosts.
  4.2 Integração com o Nmap: Por estar associado ao projeto Nmap, ele se beneficia de algumas otimizações de rede e estabilidade.
  4.3 Tempo de Execução: O Ncrack permite que os testadores definam o tempo de execução e a intensidade do ataque usando a opção -T (semelhante ao Nmap), o que é útil para evitar ser detectado por sistemas de prevenção de intrusão (IPS) ou para não sobrecarregar redes alvo.
5- John the Ripper: Diferente do Medusa, Hydra e Ncrack — que são projetados para ataques de força bruta online contra serviços de rede (como SSH, FTP, etc.) — o John the Ripper é uma ferramenta de quebra de senha offline. Ele é especificamente projetado para testar e quebrar senhas armazenadas em arquivos (como hashes de senha) que foram extraídos de um sistema.
6- Wpsacan: O WPScan é uma ferramenta de segurança de código aberto, mas com um foco muito mais específico do que as que você mencionou (Hydra, Medusa, Ncrack). Enquanto as outras são crackers de senha genéricos para múltiplos protocolos de rede, o WPScan é um scanner de vulnerabilidades projetado exclusivamente para instalações do WordPress.
7- Patator: A ferramenta Patator se encaixa na mesma categoria do Hydra e do Medusa: é um poderoso cracker de senhas online e uma ferramenta de força bruta modular usada em testes de penetração. O nome "Patator" é um acrônimo (que significa algo como Plenty of Amazing Things to Automate The On-line Reversing) e reflete seu design focado em ser flexível e modular para automatizar ataques de login.

# Preparação de ambiente de testes controlado (https://github.com/drnvalente/Simulado_Dio/issues/1#issue-3678116963) 
Utilizando o Virtual Box para hospedar as VMs e instalar a Distro Kali Linux e também o Metasploitable que é uma VM com a distro Ubuntu preparado para testes, ou seja, ela possui falahs de segurança propositalmente para efetuar os testes de invasão.
# Teste de portas abertas na VM comprometida
Depois de criado o ambinete verificada a conexão em rede de ambos (https://github.com/drnvalente/Simulado_Dio/issues/2#issue-3678209330).
Testando as portas vulneráveis com o nmap (https://github.com/drnvalente/Simulado_Dio/issues/3#issue-3678209540)

# Criação da listas "users.txt" "pass.txt"
Criadas as listas de usuários e senhas para efetuar o teste (https://github.com/drnvalente/Simulado_Dio/issues/4#issue-3678211491)
users.txt(https://github.com/drnvalente/Simulado_Dio/issues/5#issue-3678212334)
pass.txt(https://github.com/drnvalente/Simulado_Dio/issues/6#issue-3678212561)

# Efetuando o ataque com Medusa
Efetuado ataque conforme ensinado via linha de comando, obtive o resultado de sucesso em uma sequencia de usuário e senha conforme demostrado no video.(https://github.com/drnvalente/Simulado_Dio/issues/7#issue-3678235633)(https://github.com/drnvalente/Simulado_Dio/issues/8#issue-3678236250)
Efetuado o login na maquina via ftp conforme instruído na aula.(https://github.com/drnvalente/Simulado_Dio/issues/9#issue-3678236402)

# Simulando ataque em sistemas web utilizando o DWVA
Entrada no site com sucesso(https://github.com/drnvalente/Simulado_Dio/issues/9#issue-3678236402)
Teste de login inválido(https://github.com/drnvalente/Simulado_Dio/issues/13#issue-3678293190)
Obtendo informações necessárias no site para testar na Medusa(https://github.com/drnvalente/Simulado_Dio/issues/10#issue-3678290612)
Efetuando o ataque com a ferramenta Medusa consegui obter o resultado positivo de combinações de usuário e senha(https://github.com/drnvalente/Simulado_Dio/issues/11#issue-3678291161)
Efetuei o teste de login e obtive sucesso(https://github.com/drnvalente/Simulado_Dio/issues/12#issue-3678291250)
# Conclusão
Em todos os testes realizados no decorrer do curso inclusive os que não foram apresentados nesse resumo, identifiquei que as vulnerabilidades ocorrem além de sistemas configurados incorretamente mas principalmente por erros de usuários como uso de senhas fracas, usu de mesma senha para vários sites e aplicações, falta de instrução e conhecimento básico em segurança da informação, cabe as empresas a criação de palestras e cursos para seus funcionarios para mitigar os riscos e reduzir esse tipo de problema. 









