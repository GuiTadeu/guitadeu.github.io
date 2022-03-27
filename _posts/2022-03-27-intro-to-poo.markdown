---
layout: post
title:  "Introdução a Programação Orientada a Objetos"
date:   2022-03-27 14:00:00 +0530
---

Este post é um resumão da primeira parte do [Curso de Programação Orientada a Objetos](https://www.youtube.com/playlist?list=PLHz_AreHm4dkqe2aR0tQK74m8SFe-aGsY) do Gustavo Guanabara.

## Objetivo da POO

Aproximar o mundo digital do mundo real.

Antes a programação era em baixo nível, ou seja, uma linguagem de máquina de difícil acesso e especifica para aquele ambiente.

Após isso começaram a surgir as linguagens de alto nível no formato linear, que era lido de cima pra baixo como uma lista de compras. 

Depois veio a programação estruturada que trouxe as funções e permitiu executar pequenos trechos de código fora da ordem natural. Isso deu origem aos sistemas.

Assim surgiu a programação modular que permitia organizar dados e funcionalidades em capsulas protegidas que iriam compor sistemas cada vez maiores. Ela teve uma vida curta até chegar a POO.

## Quem criou?

- Alan Kay, formado em Matemática e Biologia
- Paixão em educação infantil
- "O computador ideal deve funcionar como um organismo vivo, cada célula se relaciona com outras a fim de alcançar um objetivo mas cada uma funciona de forma autonoma. As células poderiam também reagrupar-se para resolver um outro problema ou desempenhar outras funções"
- Suas ideias foram formuladas numa época que nem existia graduação em Informática, isso foi por volta de 1970
- Trabalhou na Xerox, onde existe até hoje setores de pesquisa (mouse, interface gráfica, padrão ethernet para redes, etc...)
- Uma de suas propostas para educação foi o Dynabook, uma tela na parte de cima e um teclado na parte de baixo. Isso na década de 70... Por isso é considerado um dos pais do notebook.
- Para dar origem ao Dynabook teve que ser criada uma linguagem de programação: Smalltalk que já tinha os conceitos de Classe, Objeto, Atributos e Métodos.
- Trabalhou na Apple, Disney e HP.

## Como a programação era?

Dados Globais -> Procedimentos

Problema: Filtrar os dados úteis para cada procedimento.

Como ficou?

Dados de Objetos -> Métodos

Os métodos vão usar os dados de seu respectivo objeto e pode haver troca de dados entre objetos.

## Vantagens (COMERNada)

**Confiável**

O isolamento entre as partes gera software seguro. Ao alterar uma parte nenhuma outra é afetada.

**Oportuno**

Ao dividir tudo em partes várias delas podem ser desenvolvidas em paralelo.

**Manutenível**

Atualizar um software é mais fácil. Uma pequena modificação vai beneficiar todas as partes que usarem o objeto.

**Extensível**

O software não é estático. Ele deve crescer para permanecer útil.

**Reutilizável**

Podemos usar objetos que criamos em outro sistema futuro.

**Natural**

Uma coisa natural é mais fácil de entender. Você se preocupa mais na funcionalidade do que nos detalhes de implementação.

## O que é um objeto?

Coisa material ou abstrata que pode ser percebida pelos sentidos e descrita por meio das suas características, comportamentos e estado atual.

## O que é uma classe?

Define os atributos e métodos comuns que serão compartilhados por um objeto.

Funciona como uma forma ou planta, ou seja, o objeto é uma instância/implementação de uma classe.

## O que é abstração?

A quantidade de atributos que um objeto pode ter pode ser grande. Quais são os que importam no momento? Isso é primordial na POO. Saber abstrair o que é necessário para resolver o problema.

## Modificadores de Visibilidade

Seguindo a ideia da UML e o Diagrama de Classes temos os seguintes modificadores de visibilidade:

**Public (+)**

A classe atual e todas as outras classes tem acesso aos atributos ou métodos.

**Private (-)**

Somente a classe atual vai ter acesso aos atributos ou métodos.

**Protected (#)**

Somente a classe atual e as suas sub-classes vão ter acesso aos atributos ou métodos.

## Conclusão

Essa foi a parte introdutória do curso que apresentou um pouco da história do paradigma e alguns conceitos como classe, objetos e abstração.
Vale ressaltar que na bibliografia escolhida pelo professor a Abstração não é considerada um pilar, nesse caso ela faz parte do encapsulamento.
Há um outro post criado para os pilares da orientação a objetos e você pode acessá-lo aqui: [Pilares da Programação Orientada a Objetos](https://guitadeu.github.io/posts/pillars-of-poo).

Bons estudos!


