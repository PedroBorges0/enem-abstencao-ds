# Instruções para Download dos Dados

Os arquivos brutos não são versionados no Git por causa do tamanho (~1GB).
Siga os passos abaixo para reproduzir o ambiente de dados localmente.

---

## 1. Microdados do ENEM 2023 (dataset principal)

1. Acesse: https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem
2. Baixe o arquivo microdados_enem_2023.zip
3. Extraia o CSV para: data/raw/enem_2023.csv

**Atencao:** o arquivo usa separador ponto-e-virgula (;) e encoding latin-1.
Ao abrir com pandas, use:

```python
df = pd.read_csv("data/raw/enem_2023.csv", sep=";", encoding="latin-1", low_memory=False)
```

---

## 2. IDHM Municipal — IBGE/PNUD (fonte externa 1)

1. Acesse: https://www.atlasbrasil.org.br/ranking
2. Baixe os dados de IDHM por municipio (ano mais recente disponivel)
3. Salve em: data/external/idhm_municipal.csv

Chave de integracao: CO_MUNICIPIO_RESIDENCIA (ENEM) = codigo IBGE do municipio

---

## 3. Censo Escolar 2023 — INEP (fonte externa 2)

1. Acesse: https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/censo-escolar
2. Baixe os microdados de escolas do Censo Escolar 2023
3. Salve em: data/external/censo_escolar_2023.csv

Chave de integracao: CO_ESCOLA (ENEM) = CO_ENTIDADE (Censo Escolar)
