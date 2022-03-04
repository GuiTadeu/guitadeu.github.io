---
layout: post
title:  "Introdução ao Prometheus e Grafana"
date:   2022-03-04 19:00:00 +0530
---

Este post é um resumão do vídeo [Introdução ao Prometheus e Grafana: Monitoramento Inteligente de Aplicações](https://www.youtube.com/watch?v=GPptIhzPBro) do canal [Full Cycle](https://www.youtube.com/channel/UCMUoZehUZBhLb8XaTc8TQrA).

## Importância dos Logs

O vídeo começa a falar sobre a importância dos logs para a entrega de valor.
Eles são úteis para:

- Corrigir bugs (principalmente em produção)
- Insights técnicos (onde otimizar, como integrar, querys, gargalos, etc...)
- Insights de negócio (quantas vendas por segundo, quais produtos mais/menos vistos, etc...)
- Alertar (notificar quando uma métrica estiver fora do esperado)
- Regras de Governança (facilitar a auditoria)

"Quem não mede não gerencia"

## Logs e sua Carreira?

- Você consegue ter uma visão 360 de tudo que acontece na aplicação?
- Hoje em dia a maturidade de um desenvolvedor também está na habilidade de definir métricas, entender as informações, ser data-driven....
- Quando você pensou que um dos grandes requisitos para você crescer na carreira seria entender de logs?
    - Mais do que um diferencial
    - Fazendo parte do workflow de diversas empresas
    - Desenvolvedores Full Cycle se responsabilizam pelas aplicações, inclusive seu monitoramento

## Prometheus

O Prometheus é um toolkit de monitoramento e alerta de sistema open-source.
Foi criado pela SoundCloud e atualmente faz parte da Cloud Native Computing Foundation sendo mantido de forma indenpendente.

## Conceitos Iniciais: Push vs Pull

O Prometheus trabalha utilizando o conceito de Pull.
Existem duas formas de monitorar uma aplicação:

#### Push

Precisamos ter um agent dentro da aplicação. Esse agente é o responsável por mandar as informações para o serviço monitor.

Aplicação -> Push via HTPP -> Serviço Monitor

### Pull

O serviço monitor é o responsável por ir buscar a informação na aplicação.

Serviço Monitor -> Pull via HTTP -> Aplicação (/metrics)

Você adapta sua aplicação ao formato do Prometheus.
Isso te faz pensar melhor em quais logs realmente são importantes.

## Informações relevantes em relação a aplicação

Nesse trecho é citado algumas dicas de métricas relevantes como:

- Quantidade de compras
- Tempo de resposta no processo de compra 
- Quantidade de usuários logados
- Utilização da feature X
- Busca específica no site

## E quando não foi você que desenvolveu a aplicação?

Vamos supor que queira puxar métrica de um banco MySQL ou um servidor Linux como isso seria feito?
Com o Prometheus temos uma camada chamada de exporter que fica do lado do servidor e serve como um intermediário:

Prometheus -> Pull via HTTP -> Exporter (/metrics) -> MySQL

Existem diversos Exportes já prontos para serem utilizados, raramente eles precisam ser criados.

## Métricas

### Counter

O Counter é um valor incremental, ou seja, não diminui - só acumula.
O Prometheus consegue absorver falhas no caso desse número ter um eventual reset.
Exemplo de métricas utilizando o Counter:

- Quantidade de visitas em um site
- Quantidade de vendas
- Quantidade de erros
- Etc...

### Gauge

Diferente do Counter o Gauge possui variações com o tempo, ou seja, pode aumentar ou diminuir.
Exemplo de métricas utilizando o Gauge:

- Quantidade de usuários online
- Quantidade de servidores ativos
- Etc...

### Histogram

Baseado em amostras. Seu principal diferencial é agregar valores.
Exemplo de métricas utlizando o Histogram:

- Clientes de 18-25 fizeram 15 compras no site
- Clientes de 26-35 fizeram 50 compras no site
- Etc...

### Summary

Semelhante ao Histogram mas consegue agrupar mais informações.
Exemplo de métricas utilizando o Summary:

- 50 % dos clientes de 18 a 25 fizeram compras entre Janeiro e Março
- Clientes de 35 a 40 compraram produto X na 2 últimas Quarta-feiras às 21h50
- Etc...

O vídeo não foi mais afundo no assunto de métricas pois podemos criá-las e adaptá-las e isso acaba tornando quase infinita as possibilidades.

## PromQL

É como se fosse um SQL do Prometheus. Serve para fazer consultas nos logs.
Alguns dos exemplos citados no vídeo:

- http_requests_total
- http_requests_total{status!~"4.."}
- Etc...

## O que é o Grafana?

O Grafana é uma plataforma open-source para observação de dados de forma amigável e totalmente personalizável. É possível criar dashboard em tempo real e mecanismos de alertas para eventuais falhas.

## Conclusão

Após o conteúdo inicial o vídeo cai numa parte prática que recomendo ver.
No mais caso queira mais informações sobre o Grafana recomendo a seção de tutoriais presente no site oficial. Lá tem assuntos bacanas desde os fundamentos e criação de usuários e times até a criação de plugins e instalação num Raspberry PI.

Deixarei o link da página a seguir:

<https://grafana.com/tutorials/>

Bons estudos!

