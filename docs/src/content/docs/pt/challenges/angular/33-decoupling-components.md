---
title: 🟠 Desacoplando Componentes
description: O Desafio 33 é sobre desacoplar dois componentes fortemente acoplados, usando Injeção de Token.
author: thomas-laforge
contributors:
  - tomalaforge
  - jdegand
  - LMFinney
  - Wilson-Barbosa
challengeNumber: 33
command: angular-decoupling-components
sidebar:
  order: 106
---

> Muito obrigado a **Robin Goetz** e ao seu [Spartan Project](https://github.com/goetzrobin/spartan).
> Este desafio foi proposto por Robin e é profundamente inspirado pelo seu projeto.

## Informação

O objetivo deste desafio é o de separar o comportamento de um componente do seu estilo. Neste desafio você trabalhará com um elemento botão. Quando nós clicarmos nele, nós alteraremos a propriedade _disabled_ que irá mudar estilo do elemento. Isso é um tanto quanto inútil na vida real, mas o desafio almeja demonstrar um conceito útil.

O comportamento do componente (referido como _brain_ na Spartan stack) está localizado na biblioteca brain. A parte do estilo (referida como _helmet_) está localizada dentro da biblioteca helmet. Ambas as bibliotecas não podem depender uma da outra, porque nós queremos ser capazes de publicá-las separadamente. Para nos ajudar a resolver o problema, nós estamos usando a regra eslint do Nx `enforce-module-boundaries`. Você pode encontrar mais detalhes [aqui](https://nx.dev/core-features/enforce-module-boundaries).

No entanto, o botão do helmet precisa acessar o estado do componente para, então, estilizar o botão de maneira diferente baseado no seu estado. Como mencionado acima, nós não podemos importar a diretiva `BtnDisabledDirective` diretamente na biblioteca helmet como é feito atualmente. Se você navegar até [`BtnHelmetDirective`](../../libs/decoupling/helmet/src/lib/btn-style.directive.ts), você encontrará um erro de linting. **Um projeto marcado com `type:hlm` só pode depender de bibliotecas marcadas com `type:core`**.

## Declaração

O objetico deste desafio é o de encontrar uma maneira de desacoplar as duas Diretivas.

### Dica

<details>
  <summary>Dica 1</summary>
  Leia atentamente o título do desafio 😇
</details>
