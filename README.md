README — Desafio 1: Verificador de Maioridade 🆔
📌 Sobre a atividade

Nesta atividade foi desenvolvido um sistema em PHP chamado Verificador de Maioridade.

O objetivo é criar um formulário que solicite o nome e o ano de nascimento do usuário. O sistema calcula automaticamente a idade e verifica se a pessoa é maior de idade.

🎯 Objetivos
Criar um formulário utilizando PHP e HTML.
Solicitar o Nome do usuário.
Solicitar o Ano de Nascimento.
Calcular a idade do usuário.
Verificar se o usuário possui 18 anos ou mais.
Exibir uma mensagem de acesso permitido ou negado.
Registrar os dados dos usuários maiores de idade em um arquivo de texto.
💻 Tecnologias utilizadas
PHP
HTML
Arquivo TXT para armazenamento dos acessos
📂 Estrutura do projeto
desafio1/
│
├── 5a_desafio1.php
└── log_acessos.txt
5a_desafio1.php

É o arquivo principal da atividade. Nele está o formulário e toda a lógica responsável por calcular a idade e verificar a maioridade.

log_acessos.txt

É o arquivo utilizado para registrar os dados dos usuários que possuem 18 anos ou mais.

⚙️ Funcionamento

O usuário preenche:

Nome
Ano de Nascimento

Depois, o sistema calcula a idade utilizando o ano atual.

✅ Usuário maior de idade

Se a idade for 18 anos ou mais, o sistema exibe:

Acesso permitido, [Nome]!

Além disso, os dados são registrados no arquivo:

log_acessos.txt
❌ Usuário menor de idade

Se a idade for menor que 18 anos, o sistema exibe:

Acesso negado, [Nome]!

Nesse caso, os dados não são registrados no arquivo de log.

🧮 Exemplo
Entrada
Nome: João
Ano de Nascimento: 2000
Resultado
Acesso permitido, João!

E o arquivo log_acessos.txt recebe uma informação semelhante a:

Nome: João | Ano de nascimento: 2000 | Idade: 26
🚀 Como executar
Coloque os arquivos 5a_desafio1.php e log_acessos.txt dentro da pasta do projeto.
Inicie um servidor PHP, como XAMPP, WAMP ou o servidor interno do PHP.
Abra o arquivo 5a_desafio1.php no navegador.
Preencha o nome e o ano de nascimento.
Clique em Verificar.
Confira a mensagem exibida e, quando aplicável, o registro criado em log_acessos.txt.
📚 Conceitos praticados

Nesta atividade foram praticados conceitos importantes de desenvolvimento web com PHP:

Formulários HTML
Método POST
Variáveis em PHP
Condições if e else
Cálculos com datas
Manipulação de arquivos
file_put_contents()
date()
Exibição de informações no HTML
👨‍💻 Conclusão

O Desafio 1 — Verificador de Maioridade demonstra como utilizar PHP para receber informações de um formulário, processar os dados e tomar decisões com base na idade do usuário.

A atividade também apresenta o uso de arquivos de texto para armazenar informações, permitindo praticar conceitos básicos de entrada, processamento e armazenamento de dados.
