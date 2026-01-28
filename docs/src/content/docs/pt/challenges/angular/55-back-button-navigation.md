---
title: 🟠 Back-Button-Navigation
description: O Desafio 55 é sobre substituir a navegação do botão de voltar do navegador
author: Ioannis-Tsironis
contributors:
  - tsironis13
  - Wilson-Barbosa
challengeNumber: 55
command: angular-back-button-navigation
sidebar:
  order: 123
---

## Informação

O objetivo deste desafio é substituir o comportamento padrão do botão de voltar do browser em Aplicações Angular.

Nos foi pedido, pelo time do PO, uma implementação específica quando o componente dialog está sendo exibido e o botão de voltar nativo do browser é clicado. Atualmente, o comportamento padrão do Angular, quando o botão de voltar nativo é clicado, é o de remover o histórico atual e voltar para a rota anterior.

O estado inicial da aplicação é o seguinte:
Quando qualquer dialog está sendo exibido o botão de voltar é clicado qualquer dialog aberto é fechado, e o aplicativo redireciona para a página anterior.

Este comportamento deve ser alterado, de acordo com o seguintes requisitos:

1. O requisitos ditam alguns comportamentos diferentes dependendo do tipo de dialog que está atualmente visível.
2. Por exemplo, nós temos um simples dialog de ação que deve ser fechado quando o botão de voltar for clicado, mas nós **DEVEMOS** permanecer na rota atualmente visitada (/simple-action).
3. Além disso, nós temos dialogs sensitivos como o que está na página '/senstive-action', que deve abrir um dialog de confirmação no clique do botão de voltar.
4. O dialog de confirmação, em combinação com clique no botão de voltar, deve se comportar como o dialog de ação; o dialog de confirmação deve ser fechado e nós devemos permanecer na página '/sensitive-action' com o dialog inicial ainda visível

## Declaração

Crie uma abordagem genérica e abstrata para lidar com qualquer tipo de comportamento de dialog quando o botão de voltar nativo do browser for clicado.
Alguns padrões de design do Typescript, em combinação com funcionalidades do Angular, podem ser utilizadas para suportar esse tipo de infraestrutura.

## Restrições

- A implementação não deve ser estática dependendo somente dos 2 tipos de dialog apresentados nesse desafio, mas sim escalável para suportar novos requisitos de comportamento que podem aparecer no futuro.

### Dica

<details>
  <summary>Dica 1</summary>

Use a guarda funcional `CanDeactivate`

</details>

<details>
  <summary>Dica 2</summary>

Documentação para o Material Design dialog pode ser encontrada [aqui](https://material.angular.io/components/dialog/overview)

</details>
