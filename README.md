# 📊 Annual Meeting - Mapa Escolar 2024

Este é um aplicativo desenvolvido com [Streamlit](https://streamlit.io/) que permite visualizar dados escolares para o planejamento do **Annual Meeting 2024**, com foco em oportunidades de **upsell** e análise da base atual de produtos contratados por cada escola.

## 🚀 Funcionalidades

- Proteção por senha (com uso do `st.secrets`)
- Upload e leitura de um arquivo Excel com dados escolares
- Filtro por parte do nome da escola
- Exibição de:
  - Quantidade de alunos por segmento (EI, EFI, EFII, EM, PV)
  - Marcas contratadas
  - Produtos da escola
  - Novas soluções sugeridas para upsell

## 🖼️ Interface

Ao digitar parte do nome de uma escola, o app exibe métricas segmentadas por etapa de ensino e mostra todos os produtos educacionais já contratados. Também são apresentadas soluções recomendadas para expansão de portfólio.

## 📁 Estrutura esperada do arquivo `dados.xlsx`

O Excel deve conter pelo menos as seguintes colunas:

- `School Name`
- `Alunos Educação Infantil`
- `Alunos Educação Anos Iniciais`
- `Alunos Educação Anos Finais`
- `Alunos Ensino Médio`
- `Alunos Pré Vestibular`
- Colunas adicionais com os nomes das marcas e produtos contratados pela escola

> Obs: as colunas de produtos são selecionadas com base em seus índices. Se a estrutura for alterada, ajustes no código podem ser necessários.

## 🔐 Autenticação

A aplicação está protegida por senha. A senha correta deve ser definida no arquivo `.streamlit/secrets.toml` com a seguinte estrutura:

```toml
password = "sua_senha_aqui"
