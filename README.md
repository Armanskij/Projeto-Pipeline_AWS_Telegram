# Projeto-Pipeline AWS/Telegram

Projeto de orquestração de pipelines de integrassão de bot do Telegram com a cloud AWS.

Este repositório contém um projeto de orquestração de pipeline de dados entre o Telegram e a AWS, com foco na conversão de dados transacionais em dados analíticos. Utilizamos serviços como AWS S3, AWS Lambda, AWS API Gateway, e AWS EventBridge para processar e analisar dados captados por bots do Telegram.
# Objetivo do Projeto

O objetivo deste projeto é transformar dados transacionais gerados por interações com um chatbot no Telegram em dados analíticos. Esse processo possibilita extrair insights valiosos, melhorar o desempenho do chatbot e compreender melhor o comportamento dos usuários. A ingestão, transformação e armazenamento dos dados são realizados de forma automatizada e escalável utilizando os serviços da AWS.

# Contexto

## Introdução ao ChatBot

Chatbots são ferramentas automatizadas que interagem com usuários através de plataformas de mensagens, como o Telegram. Esses bots podem capturar grandes volumes de dados transacionais, que, quando processados corretamente, podem revelar padrões comportamentais e outras informações úteis.

## Diferença entre Dados Transacionais e Analíticos

- Dados Transacionais: São os dados brutos gerados diretamente pela interação do usuário com o bot, como mensagens enviadas, comandos utilizados, etc.
- Dados Analíticos: São dados refinados e processados, preparados para análise, com o objetivo de extrair insights e informações estratégicas.

# Arquitetura

## Sistema Transacional

Neste projeto, o sistema transacional é representado pelo chatbot no Telegram, que captura e envia dados transacionais para a nuvem.
## Sistema Analítico

O sistema analítico é responsável por transformar os dados transacionais em dados prontos para análise. Ele é dividido em três etapas:

- Ingestão: Os dados são captados via webhook da API de bots do Telegram e armazenados no AWS S3 no formato JSON.
- ETL (Extração, Transformação e Carregamento): Os dados são processados por funções do AWS Lambda, que realizam a limpeza, deduplicação e compressão dos dados, armazenando-os em uma camada enriquecida no AWS S3.
- Apresentação: Os dados processados estão prontos para análise e podem ser acessados para gerar insights e relatórios.

# Justificativa para o Projeto

A necessidade de converter dados transacionais em dados analíticos surge para extrair insights valiosos, melhorar o desempenho do chatbot e entender melhor o comportamento dos usuários. Isso permite a otimização contínua das interações do bot e a personalização das respostas com base no comportamento dos usuários.


# Ferramentas Utilizadas

[![SQLite](https://img.shields.io/badge/SQLite-3.35.5-blue.svg)](https://sqlite.org/)
[![Boto3](https://img.shields.io/badge/Boto3-1.18.69-blue.svg)](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.4.3-blue.svg)](https://matplotlib.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.3.3-blue.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.11.1-blue.svg)](https://seaborn.pydata.org/)
[![Botocore](https://img.shields.io/badge/Botocore-1.21.69-blue.svg)](https://botocore.amazonaws.com/v1/documentation/api/latest/index.html)
[![Tabulate](https://img.shields.io/badge/Tabulate-0.8.9-blue.svg)](https://pypi.org/project/tabulate/)



