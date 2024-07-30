# CNPEM Data Extractor: Automação de Coleta e Análise de Informações

![CAPAS - PROJETOS (5)](https://github.com/user-attachments/assets/c5e20abd-b336-41b1-9349-41142e67ad15)

## Sumário
- [Descrição](#descrição)
- [Objetivo](#objetivo)
- [Instalação](#instalação)
- [Uso](#uso)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Pipeline](#pipeline)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Considerações Finais](#considerações-finais)
- [Contato](#contato)

## Descrição
O projeto "CNPEM Data Extractor" é um script desenvolvido para coletar dados automaticamente do site do Centro Nacional de Pesquisa em Energia e Materiais (CNPEM). O script utiliza técnicas de web scraping para extrair informações relevantes e estruturá-las em um formato conveniente para análise posterior.

## Objetivo
O objetivo deste projeto é automatizar a coleta de dados do site do CNPEM, facilitando o acesso e a análise de informações importantes. Isso permite aos pesquisadores e interessados obter dados atualizados de maneira eficiente e precisa.

## Instalação
Para instalar e executar o projeto localmente, siga os passos abaixo:

1. Clone o repositório:
   ```
   git clone https://github.com/Edu-png/CNPEM_scrapper.git
2. Navegue até o diretório do projeto:
    ```
    cd CNPEM_scrapper

3. Copiar código
    ```
    cd CNPEM_scrapper

4. Instale as dependências necessárias:
    ```
   Copiar código
   pip install -r requirements.txt

## Uso
1. Configure os parâmetros necessários no arquivo de configuração (caso necessário).

2. Execute o script principal para iniciar o processo de web scraping:
    ```
    python main.py
3. Os dados coletados serão armazenados no formato especificado, como CSV ou JSON, na pasta de saída.
   
## Estrutura do Projeto
    ```
    CNPEM_scrapper/
    │
    ├── data/                  # Dados coletados
    ├── src/                   # Código fonte
    │   ├── main.py            # Script principal
    │   ├── scraper.py         # Módulo de scraping
    │   └── config.py          # Configurações
    ├── requirements.txt       # Dependências
    └── README.md              # Documentação do projeto
    
## Pipeline
1. Coleta de Dados:
Utilização da biblioteca requests para realizar requisições HTTP ao site do CNPEM.
Obtenção de páginas HTML para processamento posterior.
2. Parsing de Dados:
Utilização da biblioteca BeautifulSoup para parsing do conteúdo HTML.
Extração de informações relevantes, como títulos, descrições, datas e outros detalhes específicos.
3. Limpeza de Dados:
Processamento dos dados extraídos para remover duplicatas, dados irrelevantes e normalizar formatos.
Conversão de tipos de dados para garantir consistência e facilitar a análise.
4. Armazenamento de Dados:
Estruturação dos dados limpos em formatos convenientes (CSV, JSON, etc.).
Salvamento dos dados na pasta data/ para análise posterior.
5. Análise e Visualização (Opcional):
Utilização de bibliotecas como Pandas para manipulação dos dados coletados.
Visualização dos dados através de gráficos e tabelas, utilizando bibliotecas como Matplotlib ou Seaborn.
6. Documentação e Relatório:
Geração de relatórios e documentação dos resultados e métodos utilizados.
Compartilhamento de insights e dados coletados para outros pesquisadores ou partes interessadas.
Tecnologias Utilizadas
Python: Linguagem de programação utilizada.
BeautifulSoup: Biblioteca para parsing de HTML e XML.
Requests: Biblioteca para realizar requisições HTTP.
Pandas: Biblioteca para manipulação e análise de dados.

## Considerações Finais
O projeto "CNPEM Data Extractor" oferece uma solução automatizada para a coleta de dados do site do CNPEM. Com uma interface fácil de usar e configuração simples, ele é ideal para pesquisadores que precisam de dados atualizados de forma contínua.

## 📞 Contato
- **LinkedIn:** [Eduardo Coqueiro](https://www.linkedin.com/in/eduardocoqueiro/)
- **Site:** [Eduardo Coqueiro](https://dataguy.my.canva.site/eduardo-coqueiro)
- **Kaggle:** [Eduardo Coqueiro](https://www.kaggle.com/eduardocoqueiro)

