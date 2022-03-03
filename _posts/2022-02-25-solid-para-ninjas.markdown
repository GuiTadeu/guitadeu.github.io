---
layout: post
title:  "Solid para Ninjas"
date:   2021-02-25 20:15:00 +0530
---

Este post é um resumão do livro SOLID para Ninjas - Projetando Classes Flexíveis do Maurício Aniche.

Ele ainda está em construção e irei adicionando novos conteúdos capítulo por capítulo...

## Capítulo 01 - Orientação a Objetos, para que te quero?

Neste primeiro capítulo é comentado sobre a complexidade em se criar sistemas usando POO.
Um dos trechos que mais achei interessante foi que, em um código procedural, a implementação é o que importa... Já num código POO, pensar no projeto de classes é o que mais tem valor.

"Pensar em orientação a objetos é mais do que pensar em código. É desenhar cada peça de um quebra cabeça e pensar em como todas elas se encaixarão juntas"

Também é citado problemas comuns em POO como, por exemplo, classes difíceis de mudar pois causam problemas em cascata ou problemas de reúso que obrigam o desenvolvedor a reescrever/duplicar código.

E finalizando, é dito que o livro vem justamente para ajudar a mitigar esses problemas fazendo um projeto de classes bem feito com base nos pilares da POO que conversam diretamente com os princípios do SOLID.

## Capítulo 02 - A Coesão e o tal do SRP

Neste capítulo é abordado o S do SOLID que é o Princípio de Responsabilidade Única.
Segue os principais pontos que são abordados:

**1. Uma classe coesa possui 1 única responsabilidade**

Direto ao ponto, se uma classe deve fazer X ela só deve fazer X.
Caso ela esteja fazendo mais do que se propõe estamos quebrando a coesão e por consequência o SRP.

**2. Uma classe não coesa tem N motivos para continuar crescendo**

Caso sua classe aumente de tamanho conforme o tempo isso pode significar que ela tem mais responsabilidades do que deveria. Para resolver isso deve-se dividir a responsabilidade com outras classes.

**3. Métodos privados não resolvem coesão de classes**

Podemos cair na tentação de querer separar a classe em funções internas.
Os métodos privados são úteis para melhorar a legibilidade do código mas caso sua classe realmente esteja com problemas de coesão siga o tópico 2 e divida com outras classes.

**4. Métodos públicos grandes demais podem se tornar classes**

Métodos públicos expõem, geralmente, dados da sua classe mãe. Se ele começar a ficar grande também é um indício de que a classe e o método tem mais responsabilidades do que deveriam. Nesse caso, talvez vale a pena extraír o método para uma classe.

**5. CTRL + F para propagar mudanças pode ser code smell**

Quando você altera uma classe e precisa usar CTRL + F constantemente para fazer a mesma alteração em N pontos do código pode significar falha na coesão.

Geralmente quer dizer que você tem a mesma responsabilidade replicada em diversos pontos do código.
Se há 4 classes, por exemplo, com um comportamento interno muito semelhante, podemos encapsular/isolar esse comportamento em 1 única classe.

Dessa forma deixamos a responsabilidade centralizada, facilmente reutilizável e alterável.

**6. Dois comportamentos pertencem a mesma responsabilidade se ambos mudam juntos**

Caso a alteração em um método A altere o funcionamento em um método B pode significar que eles possuem a mesma responsabilidade. Isso é o que chamamos de efeito colateral e que deve ser evitado com todas as suas forças.

Caso perceba isso no código refatore os comportamentos para que um não interfira no outro. Separe que o que há de comum entre os dois em um outro ponto de código.

**7. Procurando classes não coesas**

Como pode perceber acima, temos alguns pontos em comum de classes com baixa coesão:

- Muitos métodos
- Modificadas frequentemente
- Não param de crescer

Procure por esses pontos no seu projeto e busque refatorar para corrigi-los.

**8. Entender o domínio ajuda a identificar problemas de coesão**

Esse tópico tem muito a ver com abstração. Se abstrairmos demais corremos o risco sério de quebrar a coesão.

Por exemplo, para um sistema de RH (geralmente) não importa se o funcionário prefere Playstation ou Xbox.
Logo não precisamos dessa informação para cadastrar um novo colaborador.

Entender o que é necessário e o que não é ajudam a identificar problemas de coesão.
Em outras palavras, sabendo que o videogame preferido do usuário, em tese, não deveria fazer parte do cadastro dele você
facilmente identificaria um problema de coesão caso encontrasse esse atributo perdido na classe.

**9. Problemas simples == if simples**

Projetar classes é um desafio tremendo pois até quando achamos estar fazendo a coisa certa, podemos não estar.
Muitas vezes podemos criar classes ultra flexíveis, com alto reúso, baixo acoplamento, etc e tal...
Mas esquecemos que tudo isso também possuí um trade-off.

Se por um lado é bom termos classes coesas, por outro podemos tornar as coisas mais complexas do que o necessário (overengineering).

Resumidamente, problemas simples podem/devem ser resolvidos de forma simples.
Ficar pensando no que a sua aplicação vai suportar daqui a 10 anos não irá ajudar em nada.

Comece no básico e vai evoluindo/refatorando conforme achar necessidade.

**10. Não iremos conseguir escrever classes coesas o tempo inteiro**

E para finalizar o capítulo, um trecho bem bacana diz que "código de qualidade é incremental".
Ou seja, modelamos depois observamos, aprendemos e depois melhoramos.

Está tudo bem não acertar de primeira.

O importante é saber que sempre se pode melhorar...

##  Capítulo 03 - Acoplamento e o tal do DIP

Em breve...