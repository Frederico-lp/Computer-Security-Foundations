# Trabalho realizado na Semana #3
# Grupo 5 Turma 1 - CVE-2021-32244

## Indíce
- Identificação
  
- Catalogação
  
- Exploit
  
- Ataques

## Identificação
- Improper Neutralization of Input During Web Page Generation (Cross-site Scripting)
  
- Moodle versão 3.10.3
  
- Permite atacantes remotos executar web scripts ou HTML arbitrários pelo campo "Descrição".
## Catalogação
- Data de criação do relatório: 07/05/2021
  
- Nível de gravidade: Médio 5.4 (https://nvd.nist.gov/vuln/detail/CVE-2021-32244); 3.5 (https://www.cvedetails.com/cve/CVE-2021-32244/)
  
- Reportado pela primeira vez por: https://github.com/langkexiansheng em https://github.com/langkexiansheng/Images/blob/master/moodle_xss.gif

- Bug bounty: Não existem relatos de Bug Bounty.

## Exploit
- Tipo de exploit: Cross-site scripting não persistente. Para este acontecer é necessário:
    -Dados não confiaveis entrarem na aplicaçao web, na forma de web request.
    -A aplicação web gerar dinamicamente uma pagina web com estes dados não confiáveis.
    -Durante a geração da pagina, a aplicação não impede os dados apresentados de conter conteudo executável pelo browser.
  
- Tipo de automação: Não existem relatos de automação desta vulnerabilidade.

## Ataques
- Relatos de utilização da vulnerabilidade para ataques bem sucecidos: Não existem relatos de utilização desta vulnerabilidade.

- Danos potenciais:
  - Acesso a informação guardada nos cookies de utilizador
  - Criar pedidos em nome do utilizador
  - Combinado com outras falhas, é possível correr código arbitrário no computador da vítima

