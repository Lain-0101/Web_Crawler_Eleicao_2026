Web Crawler Eleição 2026 --- Maranhão
Instituição: UNIFACIMP Wyden
Curso: Engenharia de Software e Análise e Desemvolvimento de Sitemas 
Disciplina: Engenharia de Software
Atividade: Manifesto Ágil e Extreme Programming (XP)
Integrantes: Sayuri de Araujo e Maria Rita Maracaipe
Repositório: https://github.com/Lain-0101/Web_Crawler_Eleicao_2026
1. Objetivo do projeto
O projeto consulta arquivos públicos de resultados eleitorais
disponibilizados pelo Tribunal Superior Eleitoral (TSE). A aplicação
apresenta um menu para selecionar uma cidade do Maranhão, um cargo e o
turno da eleição, e então tenta consultar os dados correspondentes para
exibir candidatos, votos e situação eleitoral.

O trabalho tem como objetivo melhorar a execução, a legibilidade e as
mensagens apresentadas ao usuário, além de aplicar princípios do
Manifesto Ágil e práticas de Extreme Programming (XP).
2. Funcionalidades
- Menu interativo para selecionar São Luís, Imperatriz ou Caxias.
- Seleção do cargo: Governador, Senador, Deputado Federal ou Deputado
  Estadual.
- Seleção de primeiro ou segundo turno, conforme a disponibilidade dos
  dados e as regras implementadas.
- Consulta de arquivos JSON publicados no endereço de resultados do
  TSE.
- Exibição dos candidatos identificados, partido, quantidade de votos
  e situação.
- Destaque visual para candidatos cujo registro de dados indica
  eleição.
- Mensagens para casos em que não é possível acessar os arquivos ou
  identificar candidatos.
Escopo atual: a versão documentada disponibiliza três cidades no
menu. Portanto, ela não implementa a consulta automática de todos os
municípios do Maranhão, requisito que aparece na proposta original da
atividade.
3. Tecnologias utilizadas
- Python 3.
- Biblioteca padrão do Python: json, urllib.request e
  urllib.error.
- Arquivos JSON publicados pelo Tribunal Superior Eleitoral (TSE).
- Git e GitHub para controle de versão e compartilhamento do código.
4. Pré-requisitos
- Linux ou outro ambiente com Python 3 instalado.
- Acesso à internet para consultar os arquivos do TSE.
- O arquivo tse-top-candidates salvo no diretório do projeto.
Para verificar se o Python 3 está instalado, execute:
python3 --version
5. Como executar
Entre na pasta do projeto e execute:
python3 -u tse-top-candidates
O parâmetro -u faz com que a saída seja exibida sem atraso. Depois de
iniciar, siga as opções apresentadas no terminal:
1. Escolha uma cidade digitando o número correspondente e pressionando
   Enter.
2. Escolha o cargo.
3. Escolha o turno.
4. Aguarde a consulta e confira os resultados exibidos.
Também é possível tornar o arquivo executável:
chmod +x tse-top-candidates
./tse-top-candidates
Se a execução direta não funcionar no ambiente, use
python3 -u tse-top-candidates.
6. Fonte dos dados
Os dados são consultados nos arquivos JSON públicos do TSE, hospedados
em:

https://resultados.tse.jus.br/oficial/

A consulta depende da disponibilidade dos arquivos, da conexão com a
internet e da estrutura dos dados publicados pelo TSE. A aplicação não
cria nem altera os resultados eleitorais; ela apenas tenta consultar e
apresentar as informações recebidas.
7. Melhorias e tratamento de erros
A versão atual inclui as seguintes melhorias de implementação:
- Menus com opções numeradas e validação da opção digitada.
- Separação do código em funções para organizar a seleção de opções,
  consulta dos arquivos e apresentação dos resultados.
- Tratamento de falhas de conexão, erros HTTP, JSON inválido e
  interrupção da execução.
- Mensagens de erro para ajudar a identificar quando os dados não
  podem ser consultados.
- Exibição organizada das informações dos candidatos.
- Destaque visual para registros identificados como eleitos nos dados
  recebidos.
A identificação de eleito depende dos campos presentes no arquivo
consultado. Os dados devem ser conferidos com a publicação oficial do
TSE quando forem usados para fins informativos.
8. Aplicação do Manifesto Ágil
O Manifesto Ágil valoriza indivíduos e interações, software em
funcionamento, colaboração e resposta a mudanças. Neste projeto, esses
valores podem ser relacionados às seguintes práticas:
- Software em funcionamento: executar o programa no terminal e
  conferir se os menus e resultados são exibidos.
- Resposta a mudanças: ajustar o programa quando os testes revelam
  problemas de execução.
- Simplicidade: manter menus objetivos e uma quantidade reduzida
  de opções.
- Colaboração: revisar conjuntamente as alterações e discutir os
  problemas encontrados.
- Feedback frequente: testar novamente depois de corrigir um erro,
  em vez de deixar toda a validação para o final.
9. Práticas de Extreme Programming (XP)
A atividade propõe o uso de Pair Programming, feedback rápido, pequenas
melhorias e integração frequente.

No Pair Programming, uma pessoa atua como Driver, responsável por
digitar e implementar, enquanto a outra atua como Navigator,
responsável por revisar, identificar problemas e sugerir melhorias. Os
papéis devem ser alternados durante o trabalho.

As mudanças devem ser feitas em etapas pequenas. Após cada alteração
relevante, o programa deve ser executado para verificar se continua
funcionando. As alterações concluídas devem ser registradas em commits
com mensagens claras.

Registro da dupla: Sayuri de Araujo e Maria Rita Maracaipe. Para que
o relatório reflita fielmente o trabalho realizado, a dupla deve
confirmar e, se necessário, complementar quais etapas cada integrante
implementou ou revisou e como ocorreu a alternância entre Driver e
Navigator.
10. Validação realizada
Durante a validação manual, foi executado o programa pelo terminal e
confirmada a apresentação do menu interativo. Após ajustar a forma de
execução, a dupla informou que o programa passou a exibir os resultados
esperados.

Para uma validação completa, recomenda-se testar: - As três cidades
disponíveis no menu. - Todos os cargos oferecidos. - Primeiro e segundo
turno, quando houver dados disponíveis. - Opções inválidas digitadas no
menu. - Falta de conexão com a internet. - Arquivo de resultados
indisponível ou em formato inesperado.

Os testes adicionais devem ser executados e registrados pela dupla antes
da entrega final.
11. Limitações conhecidas
- O menu atual oferece São Luís, Imperatriz e Caxias, não todos os
  municípios do Maranhão.
- A consulta depende da disponibilidade e do formato dos arquivos
  públicos do TSE.
- O segundo turno pode não ter dados para todos os cargos ou
  localidades. A aplicação deve informar quando a consulta não estiver
  disponível.
- A indicação de eleito depende dos campos presentes nos dados
  retornados e não substitui a conferência oficial.
12. Controle de versão
O repositório do projeto é:

https://github.com/Lain-0101/Web_Crawler_Eleicao_2026

13. Conclusão
O projeto pratica conceitos de Engenharia de Software ao organizar uma
consulta interativa aos dados eleitorais do TSE, melhorar as mensagens
de execução e realizar testes no terminal. O uso de princípios ágeis e
de XP incentiva a colaboração, a simplicidade, a revisão contínua e a
correção de problemas em ciclos curtos.

Para aderir integralmente ao requisito funcional original da atividade,
ainda é necessário ampliar a consulta para todos os municípios do
Maranhão e validar separadamente a disponibilidade dos dados de cada
turno.
14. Referências
- Repositório do projeto:
  https://github.com/Lain-0101/Web_Crawler_Eleicao_2026
- Tribunal Superior Eleitoral (TSE), resultados eleitorais:
  https://resultados.tse.jus.br/oficial/
- Manifesto Ágil, princípios em português:
  https://agilemanifesto.org/iso/ptbr/principles.html
- Extreme Programming Alliance, informações sobre XP:
  https://extremeprogrammingalliance.com/about-extreme-programming-xp/