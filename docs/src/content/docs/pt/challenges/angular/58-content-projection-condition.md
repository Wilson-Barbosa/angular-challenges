---
title: 🟠 Content Projection Condition
description: O Desafio 58 é sobre projecão de conteúdo condicional no Angular
author: thomas-laforge
contributors:
  - tomalaforge
  - Wilson-Barbosa
challengeNumber: 58
command: angular-content-projection-condition
sidebar:
  order: 124
---

## Informação

Projeção de conteúdo no Angular permite que você crie componentes flexíveis e reutilizáveis, inserindo dinamicamente conteúdo de um component pai usando `<ng-content>`. No entanto, solucionar erros de projeção de conteúdo pode ser, algumas vezes, difícil.

Neste desafio, nós temos um `CardComponent` que suporta um pequeno modo, o qual muda condicionalmente como o conteúdo projetado é exibido. No entanto, há um erro: quando "small" é `falso` o card não é renderizado adequadamente.

A sua tarefa é identificar e corrigir este problema sem adicionar `inputs` enquanto garante que o comportamento desejado permanece intacto.

## Declaração

O seu objetivo é corrigir o problema em que o `CardComponent` não é renderizado quando `small` é `falso`.

## Passos para completar:

- Analize como a propriedade `small` é usada dentro do template.
- Identifique por que o conteúdo não é exibido quando `small` é `falso`.
- Modifique o componente para garantir que ambos os casos (`small` = `verdadeiro` e `small` = `falso`) funcionem como é esperado, enquanto mantém a mesma estrutura e comportamento.
- Garanta que nenhum nova propriedade `input` seja introduzida no componente.

## Restrições

- Você não deve adicionar uma nova propriedade `input`.
- A UI e o comportamento esperados devem permanecer inalterados.
- A diretiva `@if` deve ser corretamente tratada para garantir que a projeção de conteúdo funcione.
- Não introduza nenhum serviço ou administração de estado adicionais.
- A correção deve ser mínima e focada em resolver o problema de renderização.
