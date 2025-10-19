# TP01 – Integração de Sistemas de Informação (ISI)
## Licenciatura em Engenharia de Sistemas Informáticos — IPCA (2024/2025)

### 👤 Autor
**Nome:** Gonçalo Santos  
**Número:** 27985  
**Unidade Curricular:** Integração de Sistemas de Informação (ISI)  
**Instituição:** Instituto Politécnico do Cávado e do Ave (IPCA)  
**Docente:** Prof. Doutor [Nome do Professor]  
**Ano Letivo:** 2024/2025  

---

## 📘 Descrição Geral do Projeto

O presente trabalho prático consiste na **análise, desenvolvimento e implementação de um processo ETL completo**, recorrendo à ferramenta **Pentaho Data Integration (Kettle)**, com o objetivo de integrar e analisar **dados oceanográficos e informações de praias** da região de Esposende.

A solução permite:
- Extrair dados de **múltiplas fontes** (API `marine-api.open-meteo.com` e ficheiro `Praias.csv`);
- Realizar **validação e limpeza** de dados com expressões regulares (ER);
- Executar **operações de transformação** e cálculo de métricas derivadas (e.g., energia das ondas);
- Detetar **anomalias** e enviar **alertas automáticos por email**;
- Carregar os dados integrados num *data warehouse* PostgreSQL (`marine_esposende_dw`);
- Visualizar os resultados numa *Dashboard* interativa em **Node-RED**, para análise em tempo real.

---

## 🧩 Estrutura dos Ficheiros

| Pasta | Descrição |
|--------|------------|
| `doc/` | Contém o relatório final em PDF. |
| `dataint/` | Contém todas as transformações (`.ktr`) e o job principal (`.kjb`) utilizados no processo ETL. |
| `data/input/` | Contém os ficheiros de dados de entrada, nomeadamente `Praias.csv`. |
| `data/output/` | Contém ficheiros de saída, como `praias_validadas.csv`. |
| `src/` | Contém código adicional, caso exista (e.g., scripts SQL, Python). |

---

## ⚙️ Ferramentas Utilizadas

| Ferramenta | Finalidade |
|-------------|-------------|
| **Pentaho Data Integration (Kettle)** | Desenvolvimento e execução dos processos ETL. |
| **PostgreSQL 16.3** | Armazenamento do *data warehouse* `marine_esposende_dw`. |
| **Node-RED + Dashboard** | Visualização interativa e analítica dos dados oceanográficos. |
| **VS Code / DBeaver** | Apoio à edição e verificação da base de dados. |
| **YouTube** | Hospedagem do vídeo de demonstração do projeto. |

---

## 🚀 Instruções de Execução

1. **Abrir o projeto no Pentaho Data Integration (Spoon):**
   - Executar o *Job* principal: `Job_Marine_ETL.kjb`
   - Verificar as transformações:
     - `
