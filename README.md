# Projeto-Pipeline AWS/Telegram

Projeto de orquestração de pipelines de integrassão de bot do Telegram com a cloud AWS.

Este repositório contém um projeto de orquestração de pipeline de dados entre o Telegram e a AWS, com foco na conversão de dados transacionais em dados analíticos. Utilizamos serviços como AWS S3, AWS Lambda, AWS API Gateway, e AWS EventBridge para processar e analisar dados captados por bots do Telegram.
# Objetivo do Projeto

O objetivo deste projeto é transformar dados transacionais gerados por interações com um chatbot no Telegram em dados analíticos. Esse processo possibilita extrair insights valiosos, melhorar o desempenho do chatbot e compreender melhor o comportamento dos usuários. A ingestão, transformação e armazenamento dos dados são realizados de forma automatizada e escalável utilizando os serviços da AWS.

# Contexto

## Introdução ao ChatBot

Chatbots são ferramentas automatizadas que interagem com usuários através de plataformas de mensagens, como o Telegram. Esses bots podem capturar grandes volumes de dados transacionais, que, quando processados corretamente, podem revelar padrões comportamentais e outras informações úteis.

## Diferença entre Dados Transacionais e Analíticos

- **Dados Transacionais**: São os dados brutos gerados diretamente pela interação do usuário com o bot, como mensagens enviadas, comandos utilizados, etc.
- **Dados Analíticos**: São dados refinados e processados, preparados para análise, com o objetivo de extrair insights e informações estratégicas.

# Arquitetura

[![Imagem Pipeline](https://github.com/Armanskij/Projeto-Pipeline_AWS_Telegram/blob/main/Profissao%20Analista%20de%20dados%20M42%20Material%20de%20apoio%20arch.png)

## Sistema Transacional

Neste projeto, o sistema transacional é representado pelo chatbot no Telegram, que captura e envia dados transacionais para a nuvem.
## Sistema Analítico

O sistema analítico é responsável por transformar os dados transacionais em dados prontos para análise. Ele é dividido em três etapas:

- **Ingestão**: Os dados são captados via webhook da API de bots do Telegram e armazenados no AWS S3 no formato JSON.
- **ETL (Extração, Transformação e Carregamento)**: Os dados são processados por funções do AWS Lambda, que realizam a limpeza, deduplicação e compressão dos dados, armazenando-os em uma camada enriquecida no AWS S3.
- **Apresentação**: Os dados processados estão prontos para análise e podem ser acessados para gerar insights e relatórios.

# Justificativa para o Projeto

A necessidade de converter dados transacionais em dados analíticos surge para extrair **insights valiosos**, melhorar o desempenho do chatbot e entender melhor o comportamento dos usuários. Isso permite a otimização contínua das interações do bot e a personalização das respostas com base no comportamento dos usuários.


# Ferramentas Utilizadas

[![AWS S3](https://img.shields.io/badge/AWS%20S3-Storage-blue.svg)](https://aws.amazon.com/s3/)
[![AWS Lambda](https://img.shields.io/badge/AWS%20Lambda-Compute-blue.svg)](https://aws.amazon.com/lambda/)
[![AWS API Gateway](https://img.shields.io/badge/AWS%20API%20Gateway-REST%20API-blue.svg)](https://aws.amazon.com/api-gateway/)
[![AWS EventBridge](https://img.shields.io/badge/AWS%20EventBridge-Event%20Bus-blue.svg)](https://aws.amazon.com/eventbridge/)
[![Python](https://img.shields.io/badge/Python-3.8-blue.svg)](https://www.python.org/)
[![Logging](https://img.shields.io/badge/Logging-built--in-blue.svg)](https://docs.python.org/3/library/logging.html)
[![Datetime](https://img.shields.io/badge/Datetime-built--in-blue.svg)](https://docs.python.org/3/library/datetime.html)
[![Getpass](https://img.shields.io/badge/Getpass-built--in-blue.svg)](https://docs.python.org/3/library/getpass.html)
[![Requests](https://img.shields.io/badge/Requests-2.28.1-blue.svg)](https://docs.python-requests.org/)
[![Boto3](https://img.shields.io/badge/Boto3-1.28.12-blue.svg)](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
[![PyArrow](https://img.shields.io/badge/PyArrow-12.0.0-blue.svg)](https://arrow.apache.org/docs/python/)
[![PyArrow Parquet](https://img.shields.io/badge/PyArrow_Parquet-12.0.0-blue.svg)](https://arrow.apache.org/docs/python/parquet.html)





