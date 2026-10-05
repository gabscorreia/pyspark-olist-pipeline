
# Arquitetura Medalhão End-to-End (PySpark & Databricks): Olist

[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)](https://databricks.com/)
[![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)](https://spark.apache.org/)
[![Delta Lake](https://img.shields.io/badge/Delta_Lake-003366?style=for-the-badge&logo=delta-lake&logoColor=white)](https://delta.io/)
[![Git](https://img.shields.io/badge/GIT-F05032?style=for-the-badge&logo=git&logoColor=white)](https://git-scm.com/)

</div>

---

## 📌 Visão Geral do Projeto

Este repositório contém um projeto completo de engenharia de dados desenvolvido com **PySpark** no ambiente **Databricks**, utilizando dados públicos do e-commerce da Olist. O objetivo principal é estruturar um pipeline de dados robusto seguindo a **Arquitetura Medalhão** (Bronze $\rightarrow$ Silver $\rightarrow$ Gold) para garantir o processamento, transformação e entrega de camadas analíticas de alta performance.

---

## 🏗️ Arquitetura do Projeto

O pipeline foi desenhado em camadas no Databricks, garantindo rastreabilidade, limpeza rigorosa e performance:

```text
[ CSVs Olist ] ---> [ Unity Catalog Volumes ] ---> [ Camada Bronze (Raw) ] 
                                                                |
                                                                v
[ Camada Gold / ML Ready ] <--- [ Camada Silver (Processed) / Joins ]
