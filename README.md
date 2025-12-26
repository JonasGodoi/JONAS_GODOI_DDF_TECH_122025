# 🛒 Technical Case: Data Engineering Pipeline (E-commerce)

> **Candidato:** Jonas de Godoi
> **Case:** Technical Case Base v2.2 - Dadosfera

## 📋 Sobre o Projeto
Este projeto visa a construção de uma Plataforma de Dados moderna para uma empresa de E-commerce, substituindo uma arquitetura legada complexa por uma solução integrada na **Dadosfera**.

O objetivo é centralizar dados de Pedidos, Clientes e Produtos para habilitar análises descritivas (BI) e prescritivas (IA/LLMs), focando em agilidade e redução de custos.

## 🛠️ Item 0: Planejamento e Agilidade
Seguindo metodologias ágeis, o projeto foi dividido em Sprints focadas nas camadas do Data Lake.
Abaixo, o quadro de acompanhamento (Kanban) das atividades:

<img width="1918" height="915" alt="Captura de tela 2025-12-26 175658" src="https://github.com/user-attachments/assets/de9bce81-2124-4e51-b9ef-6c8b9b1d8ac9" />


*O planejamento foi estruturado para cobrir o ciclo de vida completo dos dados, desde a ingestão até a ativação com IA.*

## 🏗️ Arquitetura e Decisões Técnicas
Baseado em experiências acadêmicas anteriores (especificamente meu TCC sobre *ETL Pipelines for Traffic Data*), a solução foi desenhada priorizando:

1.  **Ingestão Híbrida:** Tratamento prévio de dados brutos (CSV) em ambiente SQL local para garantir tipagem forte e integridade relacional antes do upload para a nuvem.
2.  **Data Quality:** Uso de técnicas de validação para garantir regras de negócio (ex: preços não podem ser negativos).
3.  **Modern Data Stack:** Substituição de componentes dispersos (AWS Kinesis, Redis) por módulos nativos da Dadosfera.

## 🚀 Como reproduzir
1.  **Base de Dados:** Os dados utilizados são do [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).
2.  **Stack:**
    * **SQL (MySQL):** Para microtransformação e saneamento inicial.
    * **Dadosfera:** Para Data Lake, Catalogação e Visualização.
    * **Python/Streamlit:** Para criação do Data App.
