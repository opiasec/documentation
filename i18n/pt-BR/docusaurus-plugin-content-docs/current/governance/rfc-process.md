---
sidebar_label: 'Processo de RFC'
title: 'Processo de RFC (Request for Comments)'
---

## O que é uma RFC?

Uma RFC (Request for Comments) é a forma como propomos, discutimos e decidimos sobre mudanças significativas na nossa plataforma. Isso inclui, mas não se limita a:

* Alterações na arquitetura principal do projeto.
* Introdução de novas funcionalidades complexas.
* Mudanças em convenções de código ou processos de contribuição.
* Decisões que afetam a experiência de todos os usuários ou contribuidores.

O objetivo é ter um processo transparente, público e colaborativo para guiar a evolução do projeto, aproveitando a sabedoria coletiva da comunidade.

## O Processo Simplificado

Nosso processo é desenhado para ser ágil e se baseia no uso das **GitHub Issues**.

### Passo 1: A Proposta (Abertura da RFC)

* Qualquer pessoa pode propor uma RFC.
* Para isso, deve-se criar uma **nova Issue no GitHub** utilizando o nosso template específico **"Proposta de RFC (Request for Comments)"**.
* O template guiará o autor a fornecer todo o contexto necessário:
    * Um resumo claro da proposta.
    * A motivação e o problema que ela resolve.
    * Um detalhamento técnico da implementação sugerida.
    * As alternativas que foram consideradas.
    * As potenciais desvantagens ou riscos.

### Passo 2: A Discussão

* Uma vez que a Issue da RFC é aberta, ela entra em um período de discussão pública. O autor da RFC deve adicionar a label `rfc-discussion`.
* Toda a comunidade é encorajada a ler a proposta e deixar seus comentários, perguntas e sugestões na própria Issue.
* O autor da RFC é responsável por responder às perguntas e, se necessário, refinar a proposta com base no feedback recebido.

### Passo 3: A Decisão

* Não temos um comitê formal. A decisão é tomada com base no **consenso aproximado** entre os mantenedores do projeto, após um período razoável de discussão (geralmente, de 7 a 14 dias).
* Se a proposta for aceita, a Issue é marcada com a label `rfc-accepted` e fechada. A implementação pode então começar (geralmente através de um ou mais Pull Requests que fazem referência à Issue da RFC).
* Se for rejeitada, a Issue é marcada como `rfc-rejected`, com um comentário final explicando os motivos da recusa, e é fechada.

Este processo garante que todas as grandes decisões sejam bem documentadas, discutidas publicamente e arquivadas no GitHub para referência futura.

## Estados e Labels (Etiquetas) de uma RFC

Para facilitar a visualização e o rastreamento do ciclo de vida de uma proposta, utilizamos um conjunto padronizado de labels (etiquetas) no GitHub. Cada RFC deve ter sempre uma (e apenas uma) label de estado.

Aqui estão os estados possíveis e seus significados:

* **rfc-proposal** (Cor sugerida: cinza ⚪)
    * Estado: Proposta.
    * Descrição: Este é o estado inicial de toda RFC recém-criada. Significa que a proposta foi formalizada, mas a discussão aprofundada ainda não começou ou está em seus estágios iniciais.

* **rfc-discussion** (Cor sugerida: azul 🔵)

    * Estado: Em Discussão.
    * Descrição: A proposta está ativamente buscando feedback da comunidade e dos mantenedores. Este é o período principal para comentários, sugestões e refinamentos.

* **rfc-accepted** (Cor sugerida: verde 🟢)
    * Estado: Aceita.
    * Descrição: A proposta foi aprovada após o período de discussão e atingiu um consenso aproximado entre os mantenedores. A RFC é considerada "finalizada" e a implementação pode começar.

* **rfc-rejected** (Cor sugerida: vermelho 🔴)
    * Estado: Rejeitada.
    * Descrição: Após a discussão, a proposta foi recusada. Um comentário final dos mantenedores deve explicar os motivos da rejeição.

* **rfc-withdrawn** (Cor sugerida: laranja 🟠)
    * Estado: Retirada.
    * Descrição: O autor original da RFC decidiu retirar a proposta de consideração. Isso pode ocorrer por vários motivos, como mudança de ideia ou descoberta de uma solução melhor.

* **rfc-superseded** (Cor sugerida: `roxo` 🟣)
    * Estado: Substituída.
    * Descrição: A proposta se tornou obsoleta porque foi substituída por outra RFC mais recente e aprovada. A issue da RFC que a substituiu deve ser referenciada.
    
### Fluxo do Ciclo de Vida
O fluxo típico de uma RFC segue este caminho:

`rfc-proposal` → `rfc-discussion` → [ `rfc-accepted` | `rfc-rejected` | `rfc-withdrawn` | `rfc-superseded` ]