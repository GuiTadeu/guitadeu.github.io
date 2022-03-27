---
layout: post
title:  "Pilares da Programação Orientada a Objetos"
date:   2022-03-27 16:00:00 +0530
---

Este post é um resumão da segunda parte do [Curso de Programação Orientada a Objetos](https://www.youtube.com/playlist?list=PLHz_AreHm4dkqe2aR0tQK74m8SFe-aGsY) do Gustavo Guanabara.

Há um post introdutório que faz um resumo da primeira parte onde contém um pouco da história do paradigma. Você pode acessa-lo aqui: [Introdução a Programação Orientada a Objetos](https://guitadeu.github.io/posts/intro-to-poo).

## Encapsulamento

Ocultar partes independentes da implementação, permitindo construir partes invisíveis ao mundo exterior.

Quem vai interagir com a cápsula não precisa saber dos detalhes internos. Só é necessário uma requisição e uma resposta.

Um bom objeto encapsulado precisa fornecer uma Interface, ou seja, uma lista de serviços fornecidos por esse componente. É o contato com o mundo exterior que define o que pode ser feito com um objeto dessa classe.

### Vantagens

1. Tornar mudanças invisíveis: Uma cápsula pode ser trocada por outra desde que usem o mesmo padrão (interface)

2. Facilitar a reutilização de código: Podemos usar o código encapsulado em outros trechos do sistema

3. Reduzir efeitos colaterais: Evitando o contato do desenvolvedor com a implementação diminuimos o risco de ter problemas por alguma mudança interna. Por isso também é importante ter uma interface padrão.

## Herança

Permite basear uma nova classe na definição de uma outra classe previamente existente.

A herança será aplicada tanto para características quanto para comportamentos.

Temos a classe mãe (superclasse) e as classes filhas (subclasses)

### Árvores Hierárquicas

Não podemos afirmar que uma subclasse é sub sempre. Uma classe pode ser sub de uma e super de outra.

Quando uma classe é mãe de todas (não tem superclasse) ela é considerada a classe raíz.

Já as subclasses que não tem filhas são chamadas de folhas.

A partir do terceiro nível da hierarquia chamamos as subclasses de descendentes e as superclasses de ancestrais. Exemplo:

ACA -> AC -> A

Onde:

- A: Classe raíz, superclasse, Mãe de AC, ancestral de ACA

- AC: Filha de A (subclasse), Mãe de ACA (superclasse)

- ACA: Classe folha, Filha de AC (subclasse), descendente de A

Quando percorremos a árvore de cima pra baixo (da raíz até as folhas) chamamos de Especialização. Já o contrário é chamado de Generalização.

### Tipos de Heranças

**De Implementação**

Considerada herança pobre, a herança mais simples que tem. É quando uma classe herda e não tem nada mais a compor.

**Para Diferença**

Quando uma classe herda e adiciona mais atributos ou comportamentos.

### Abstrato e Final

**Classe Abstrata**

Não pode ser instanciada. Só pode servir como superclasse.

**Método Abstrato**

Declarado mas não implementado pela superclasse.

**Classe Final**

Não pode ser herdada por outra classe.
Obrigatoriamente é uma classe folha.

**Método Final**

Não pode ser sobrescrito pelas suas sub-classes. Obrigatoriamente herdado.

## Polimorfismo

Junção das palavras Poli (muitas) e Morfo (formas), ou seja, "muitas formas".

Permite que o mesmo nome represente vários comportamentos diferentes.

### Assinatura do método

Consiste na quantidade e os tipos dos parâmetros. Caso tenhamos o mesmo valor em ambos podemos dizer que temos a mesma assinatura.

### Tipos de Polimorfismo

**Sobreposição**
É quando sobrescrevemos o método. Geralmente usamos o @Override no Java, por exemplo. Permite fazer a mesma coisa com comportamentos diferentes.

Em outras palavras, acontece quando substítuimos um método de uma superclasse na sua subclasse usando a mesma assinatura.

Resumo: Mesma assinatura em classes diferentes.

**Sobrecarga**

Quando usamos o mesmo nome do método e alteramos os seus atributos (assinaturas diferentes) podendo assim condicionar o comportamento.

Resumo: Assinaturas diferentes na mesma classe.

## Conclusão

Essa foi a parte mais conceitual do curso (que também possuí vídeos práticos).
Nela vimos que todos os pilares estão ligados e se complementam.
Ao meu ver, a abstração seria a parte mais importante do paradigma.

Precisamos abstrair para encapsular (interfaces), herdar (abstract e final) e polimorfar (override e sobrescrita).
Por isso um bom design de classes é tão importante quanto saber os pilares.
Para isso temos o SOLID que são os pilares aplicados com boas práticas.

Recomendo a leitura sobre o assunto, já há um artigo sobre SRP aqui: [Coesão e o Princípio de Responsabilidade Única](https://guitadeu.github.io/posts/solid-srp).

Bons estudos!
