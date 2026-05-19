# Predição de Abandono no 2º Dia do ENEM

**Projeto Final — Ciência de Dados: Análise de Dados Aplicada**
Prof. Dr. Eduardo Pena

## Integrantes
- Pedro Borges De Araujo


## Problema

Aproximadamente 32% dos inscritos no ENEM 2023 não compareceram ao segundo dia de provas
(Ciências da Natureza e Matemática), representando mais de 1,25 milhão de candidatos.
Este projeto constrói um **classificador de risco de abandono** para candidatos que
compareceram ao primeiro dia, usando variáveis socioeconômicas, escolares e geográficas.

## Datasets

| Dataset | Fonte | Integração |
|---|---|---|
| Microdados ENEM 2023 | INEP / dados.gov.br | Dataset principal |
| IDHM Municipal | IBGE/PNUD / atlasbrasil.org.br | Chave: código IBGE do município |
| Censo Escolar 2023 | INEP / dados.gov.br | Chave: código da escola |

## Como Reproduzir

```bash
# 1. Clonar o repositório
git clone https://github.com/[usuario]/enem-abstencao-ds.git
cd enem-abstencao-ds

# 2. Instalar dependências
pip install -r requirements.txt

# 3. Baixar os dados (ver instruções em data/README.md)

# 4. Executar os notebooks em ordem
jupyter notebook notebooks/
```

## Status das Etapas

| Etapa | Descrição | Status |
|---|---|---|
| 1 | Definição do problema | Entregue |
| 2 | Integração e limpeza de dados | Em andamento |
| 3 | EDA e consultas SQL | Pendente |
| 4 | Modelagem com ML | Pendente |
| 5 | Relatório e apresentação | Pendente |
