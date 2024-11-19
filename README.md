# CNPEM Data Extractor: Automação de Coleta e Análise de Informações

<p align="center">
  <a href="https://github.com/Edu-png">
    <img src="https://img.shields.io/badge/Autor-Eduardo%20Coqueiro-purple?style=flat&logo=github" alt="Autor">
  </a>
  <a href="mailto:eduardocoqueiro@gmail.com">
    <img src="https://img.shields.io/badge/Email-eduardocoqueiro%40gmail.com-purple?style=flat&logo=gmail" alt="Email">
  </a>
  <a href="https://linkedin.com/in/eduardocoqueiro/">
    <img src="https://img.shields.io/badge/LinkedIn-Eduardo%20Coqueiro-purple?style=flat&logo=linkedin" alt="LinkedIn">
  </a>
  <a href="https://kaggle.com/EduardoCoqueiro">
    <img src="https://img.shields.io/badge/Kaggle-Eduardo%20Coqueiro-blue?style=flat&logo=kaggle" alt="Kaggle">
  </a>
</p>

![CAPAS - PROJETOS (5)](https://github.com/user-attachments/assets/c5e20abd-b336-41b1-9349-41142e67ad15)

## Sumário 📑

1. [Resumo 📄](#resumo-)
2. [Requisitos 🛠](#requisitos-)
3. [Introdução ☀](#introdução-)
   - [Objetivo 🎯](#objetivo-)
4. [Pipeline do Projeto 🛠](#pipeline-do-projeto-)
5. [Funcionalidades 🚀](#funcionalidades-)
6. [Metodologia 🧪](#metodologia-)
   - [1. Configuração Inicial](#1-configuração-inicial)
   - [2. Coleta de Dados](#2-coleta-de-dados)
   - [3. Raspagem de Dados](#3-raspagem-de-dados)
   - [4. Processamento dos Dados](#4-processamento-dos-dados)
   - [5. Validação](#5-validação)
   - [6. Melhorias Futuras](#6-melhorias-futuras)
7. [Resultados e Conclusões 📈](#resultados-e-conclusões-)
   - [Resultados ✨](#resultados-)
   - [Conclusões 🚀](#conclusões-)
8. [Considerações Finais 🚀](#considerações-finais-)
   - [Pontos de Destaque](#pontos-de-destaque)
   - [Limitações e Melhorias](#limitações-e-melhorias)
   - [Próximos Passos](#próximos-passos)
9. [Agradecimentos 👏](#agradecimentos-)

## Resumo 📄

Este projeto foi um dos primeiros que realizei em python e foi desenvolvido para automatizar o processo de extração de informações sobre vagas de emprego no site oficial do **CNPEM (Centro Nacional de Pesquisa em Energia e Materiais)** como parte do meu emprego na Coractium (uma startup de educação e gerenciamento de carreira para cientistas). O script utiliza técnicas de **web scraping** com a biblioteca `BeautifulSoup` para acessar a página de vagas abertas do CNPEM e coletar dados estruturados sobre as oportunidades disponíveis. As informações são processadas e organizadas em um arquivo Excel, permitindo fácil análise e visualização dos dados.

<img width="959" alt="vagas" src="https://github.com/user-attachments/assets/fea3e8c5-2868-45f6-abdd-23ffb6ab44a8">


A partir da URL principal, o código faz uma requisição à página, simula o comportamento de um navegador real através de um `User-Agent` customizado, e coleta as seguintes informações:
- **Título da Vaga:** Nome ou descrição da oportunidade.
- **Data de Publicação:** Indica quando a vaga foi publicada ou atualizada.
- **Resumo da Vaga:** Uma breve descrição com os principais requisitos ou informações sobre a vaga.

### Funcionalidades do Script:
- **Tratamento de Erros SSL:** O código desativa verificações SSL (não recomendado para produção) para facilitar a raspagem em um ambiente seguro, mas simplificado.
- **Verificação de Status HTTP:** Garante que a página foi carregada com sucesso antes de iniciar a extração de dados.
- **Exportação para Excel:** Os dados coletados são organizados em um `DataFrame` do `pandas` e exportados para um arquivo Excel chamado `vagas_cnpem.xlsx`. Este formato permite a integração com ferramentas como Power BI, Excel, ou outros scripts Python para análises adicionais.

### Possíveis Expansões e Melhorias:
1. **Suporte a múltiplas páginas de vagas.**
2. **Envio de notificações por e-mail para alertar sobre novas oportunidades.**
3. **Adição de filtros personalizados para buscar vagas específicas por área ou palavra-chave.**

Com o **CNPEM Job Scraper**, o processo de monitoramento e análise de oportunidades no site do CNPEM se torna muito mais eficiente e rápido, economizando tempo e esforço manual.

## Requisitos 🛠
Certifique-se de ter as seguintes dependências instaladas:
- Python 3.8 ou superior
- Bibliotecas:
  - `beautifulsoup4`
  - `pandas`
  - `openpyxl`
  - `requests`

## Introdução ☀

O **CNPEM Job Scraper** foi desenvolvido para automatizar a extração de dados sobre vagas de emprego no site oficial do **Centro Nacional de Pesquisa em Energia e Materiais (CNPEM)**. Utilizando técnicas de web scraping, o projeto coleta informações detalhadas sobre oportunidades abertas e as organiza em um formato estruturado para facilitar o acesso e análise.

### Objetivo 🎯
O principal objetivo deste projeto é simplificar o processo de monitoramento de vagas no site do CNPEM, economizando tempo e esforço manual. Com este script, é possível:
- Extrair informações de forma automática, incluindo títulos de vagas, datas de publicação e resumos.
- Armazenar os dados em um arquivo Excel para análises adicionais ou integração com outras ferramentas.
- Servir como base para futuras implementações, como notificações automáticas ou análise avançada das oportunidades disponíveis.

## Pipeline do Projeto 🛠

A pipeline deste projeto foi estruturada em etapas simples e organizadas para garantir a coleta, processamento e armazenamento dos dados de vagas do site do CNPEM. Abaixo estão as etapas detalhadas:

### 1. **Configuração do Ambiente**
   - Instalação das bibliotecas necessárias: `beautifulsoup4`, `pandas`, `openpyxl` e `requests`.
   - Configuração de permissões para desativar verificações SSL (somente em ambiente de desenvolvimento).

### 2. **Coleta de Dados**
   - Realiza uma requisição HTTP para acessar a página de vagas abertas no site do CNPEM.
   - Define um `User-Agent` para simular o comportamento de um navegador real, garantindo uma comunicação mais confiável com o servidor.

### 3. **Extração de Dados**
   - Utiliza a biblioteca `BeautifulSoup` para parsear o HTML da página e localizar as informações desejadas.
   - Coleta os seguintes dados:
     - **Título da Vaga**
     - **Data de Publicação**
     - **Resumo da Vaga**

### 4. **Armazenamento dos Dados**
   - Os dados extraídos são organizados em um `DataFrame` do `pandas`.
   - São salvos em um arquivo Excel (`vagas_cnpem.xlsx`) para facilitar o acesso e a análise futura.

### 5. **Validação**
   - Verifica o status da requisição HTTP para garantir que os dados foram coletados corretamente.
   - Confirma que o arquivo Excel foi gerado com sucesso no diretório do projeto.

### 6. **Possíveis Expansões**
   - Suporte para múltiplas páginas de vagas, permitindo a raspagem de um volume maior de dados.
   - Implementação de filtros automáticos para buscar vagas específicas por área ou palavra-chave.
   - Integração com notificações por e-mail para alertar sobre novas vagas.

## Funcionalidades 🚀
- Coleta informações de **títulos de vagas**, **datas de publicação** e **resumos** das oportunidades.
- Armazena os dados coletados em um arquivo Excel (`vagas_cnpem.xlsx`).
- Fácil de configurar e personalizar para outros sites de vagas, com ajustes no código.

## Metodologia 🧪

A execução deste projeto foi dividida em etapas para garantir uma abordagem sistemática e organizada no processo de extração e processamento dos dados. Abaixo, apresento os métodos utilizados:

### 1. **Configuração Inicial**
- Instalação das bibliotecas essenciais:
  - `beautifulsoup4`: Para web scraping e análise do HTML.
  - `pandas`: Para manipulação e organização dos dados em formato tabular.
  - `requests`: Para realizar requisições HTTP.
  - `openpyxl`: Para exportar os dados no formato Excel.
- Configuração de permissões e desativação de verificações SSL com a biblioteca `urllib3`, facilitando a conexão com o site do CNPEM.

---

### 2. **Coleta de Dados**
- **Requisição HTTP:** 
  - Foi feita uma requisição para a URL do site do CNPEM utilizando um `User-Agent` customizado para simular o comportamento de um navegador real.
- **Tratamento de Respostas HTTP:** 
  - Verificação do código de status para garantir que a página foi acessada com sucesso antes de iniciar o processamento.

---

### 3. **Raspagem de Dados**
- Utilizando o `BeautifulSoup`, o script parseou o HTML da página e identificou os seguintes elementos:
  - **Título da Vaga:** Extraído de elementos `<h3>`.
  - **Data de Publicação:** Localizada em elementos `<time>` com classe específica.
  - **Resumo da Vaga:** Obtido a partir de elementos `<div>` com a classe correspondente.

---

### 4. **Processamento dos Dados**
- **Organização dos Dados:**
  - Os dados coletados (título, data, resumo) foram armazenados em listas separadas.
  - Em seguida, essas listas foram combinadas em um `DataFrame` do `pandas`.
- **Exportação:**
  - O `DataFrame` foi exportado para um arquivo Excel (`vagas_cnpem.xlsx`) utilizando o módulo `openpyxl`.
  - O arquivo gerado contém as colunas:
    - **Título da Vaga**
    - **Data**
    - **Resumo**

---

### 5. **Validação**
- O script verifica:
  - A existência e o conteúdo das listas após a extração.
  - Se o arquivo Excel foi gerado com sucesso e está no formato correto.
- Tratamento de possíveis erros de conexão ou ausência de dados.

---

### 6. **Melhorias Futuras**
- Automatizar a coleta de dados para múltiplas páginas.
- Adicionar filtros para vagas específicas, como área ou data de publicação.
- Implementar notificações automáticas para alertar sobre novas oportunidades.

## Resultados e Conclusões 📈

### Resultados ✨
Após a execução do script, os dados das vagas do site do CNPEM foram coletados com sucesso e armazenados em um arquivo Excel (`vagas_cnpem.xlsx`). Os principais resultados obtidos incluem:

1. **Dados Extraídos:**
   - **Título da Vaga:** O nome ou descrição principal da oportunidade.
   - **Data de Publicação:** Indica quando a vaga foi publicada ou atualizada no site.
   - **Resumo da Vaga:** Uma breve descrição da oportunidade, incluindo requisitos ou informações importantes.

2. **Exemplo de Formato do Arquivo Gerado:**
   O arquivo Excel gerado contém as seguintes colunas organizadas:
   | Título da Vaga      | Data        | Resumo                                           |
   |---------------------|-------------|-------------------------------------------------|
   | Pesquisador Sênior  | 20/11/2024 | Oportunidade para liderar projetos inovadores. |
   | Técnico de Laboratório | 15/11/2024 | Suporte técnico em análises laboratoriais.     |

3. **Automação do Processo:**
   - O script automatizou com sucesso a coleta de dados, eliminando a necessidade de acesso manual ao site para monitorar vagas.

4. **Exportação e Organização:**
   - Os dados coletados foram organizados em um `DataFrame` do `pandas` e exportados para o formato Excel, permitindo integração com ferramentas como Power BI ou análise avançada em Python.

---

### Conclusões 🚀
O projeto **CNPEM Job Scraper** demonstrou ser uma solução eficaz para monitorar e coletar informações sobre vagas de emprego do site do CNPEM. As principais conclusões incluem:

1. **Eficiência no Processo:**
   - A automação reduziu significativamente o tempo necessário para acessar e coletar informações, tornando o monitoramento mais rápido e menos suscetível a erros humanos.

2. **Qualidade dos Dados:**
   - O script foi capaz de extrair informações precisas e organizadas, demonstrando a robustez do uso de `BeautifulSoup` para web scraping.

3. **Reusabilidade:**
   - A estrutura modular do código facilita sua adaptação para outros sites semelhantes, ampliando o alcance do projeto.

4. **Limitações Identificadas:**
   - O script atualmente funciona apenas para uma página de vagas e não possui suporte para múltiplas páginas.
   - Requer desativação de verificações SSL, o que não é recomendado para ambientes de produção.

5. **Próximos Passos:**
   - Expandir a funcionalidade para suportar múltiplas páginas de vagas.
   - Implementar notificações automáticas via e-mail para alertar sobre novas oportunidades.
   - Adicionar filtros avançados para personalizar a coleta de dados por área ou palavra-chave.

Com este projeto, foi possível não apenas automatizar a coleta de dados de vagas, mas também criar uma base sólida para futuras expansões e melhorias. A aplicação é uma ferramenta útil para quem deseja acompanhar as oportunidades no CNPEM de forma rápida e eficiente.

## Considerações Finais 🚀

O **CNPEM Job Scraper** apresentou uma solução prática e eficiente para monitorar as vagas de emprego no site do CNPEM, automatizando a coleta e organização das informações. Este projeto destacou a importância e a aplicabilidade de técnicas de web scraping para resolver problemas do dia a dia, especialmente quando há a necessidade de acessar grandes volumes de dados de maneira repetitiva.

### Pontos de Destaque:
1. **Eficiência Operacional:**
   - A automação do processo eliminou a necessidade de visitas manuais frequentes ao site, economizando tempo e esforço.
   - O uso de ferramentas como `BeautifulSoup` e `pandas` possibilitou a criação de um pipeline robusto e reutilizável.

2. **Impacto Prático:**
   - O projeto facilita o acompanhamento de novas oportunidades de emprego, especialmente para profissionais que buscam atuar no CNPEM.
   - O arquivo Excel gerado oferece uma forma acessível de organizar e visualizar os dados, podendo ser integrado a outras ferramentas para análises mais avançadas.

3. **Flexibilidade e Escalabilidade:**
   - A estrutura do código é modular e pode ser facilmente adaptada para outros sites ou requisitos específicos.
   - Há espaço para expansão, como suporte a múltiplas páginas, notificações automáticas e filtros personalizados.

### Limitações e Melhorias:
Apesar de seus benefícios, o projeto possui algumas limitações que podem ser abordadas em futuras versões:
- Atualmente, o script coleta dados apenas da primeira página de vagas.
- A desativação de verificações SSL é funcional para desenvolvimento, mas não é ideal para ambientes de produção.
- Não há filtros ou notificações automáticas, o que pode limitar o uso para acompanhamento em tempo real.

### Próximos Passos:
1. Implementar suporte a múltiplas páginas de vagas.
2. Adicionar notificações automáticas por e-mail ou outras plataformas, como Telegram ou WhatsApp.
3. Desenvolver filtros dinâmicos para buscar vagas específicas por área, data ou palavras-chave.
4. Garantir conformidade com verificações SSL para uso em ambientes de produção.

Em resumo, o projeto **CNPEM Job Scraper** mostrou como tecnologias simples e acessíveis podem ser utilizadas para criar ferramentas altamente úteis no contexto profissional. Ele serve como base para futuras aplicações e demonstra o potencial de automação de tarefas rotineiras, promovendo eficiência e praticidade.

## Agradecimentos 👏

Gostaria de expressar minha gratidão às seguintes entidades pelo suporte e contribuição para o desenvolvimento deste projeto:

- **Coractium**: Pelo apoio e orientação durante o planejamento e execução deste projeto, proporcionando uma experiência prática e desafiadora que contribuiu para meu aprendizado e crescimento profissional.
  
- **Centro Nacional de Pesquisa em Energia e Materiais (CNPEM)**: Pela disponibilização pública das informações sobre vagas de emprego, permitindo que este projeto automatizasse a coleta de dados e ajudasse a tornar as oportunidades mais acessíveis.

Este trabalho não seria possível sem o apoio dessas organizações, que desempenham um papel importante na disseminação do conhecimento e no incentivo à inovação.

<div align="center">
  <img src="https://github.com/user-attachments/assets/54afb33c-97be-40b6-8c96-0f12852e946f" alt="thank-you" width="500">
</div>

## 📞 Contato
- **LinkedIn:** [Eduardo Coqueiro](https://www.linkedin.com/in/eduardocoqueiro/)
- **Site:** [Eduardo Coqueiro](https://dataguy.my.canva.site/eduardo-coqueiro)
- **Kaggle:** [Eduardo Coqueiro](https://www.kaggle.com/eduardocoqueiro)

