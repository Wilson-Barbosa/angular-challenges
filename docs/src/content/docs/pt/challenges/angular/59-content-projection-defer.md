---
title: 🔴 content-projection-defer
description: Challenge 59 is about deferring fetching data
author: thomas-laforge
contributors:
  - tomalaforge
  - Wilson-Barbosa
challengeNumber: 59
command: angular-content-projection-defer
sidebar:
  order: 212
---

# Carregamento adiado para Conteúdo de Card Expansível

## Informação

Dentro da aplicação, especificamente na page2, há um componente card expansível. Este componente consiste em um título permanentemente visível e uma seção de conteúdo que está escondida até que o card se expanda. Esta seção de conteúdo é populada com uma lista de posts, que é obtida através de uma chamada para uma API backend. A implementação atual apresenta um problema: quando navegado para a page2, ainda que o comportamento padrão do card seja o estado colapsado, a chamada à API para carregar a lista de posts é acionada imediatamente durante o processo de carregamento da página, antes que o usuário tenha escolhido expandir o card e visualizar o conteúdo.

## Declaração

O objetivo desse desafio é otimizar o comportamento do carregamento de dados para o componente de card expansível em `page`. Modifique a implementação para que a chamada à API que busa a lista de posts seja **adiada**. Os dados devem ser **somente** buscados quando o usuário explicitamente interagir com o card para **expandí-lo**. Nenhuma busca da lista de posts deve ocorrer sob o carregamento inicial da `page2` enquanto o card permanecer colapsado.

## Restrições

- O card expansível deve reter a sua funcionalidade principal: mostrar o título, estar inicialmente colapsado (no carregameto de `page2`) e expandir e colapsar através de interação do usuário.
- Quando o card estive expandido, a lista de posts deve ser buscada no backend e exibida dentro da área de conteúdo.
- Os mecanismo de busca (isto é, o endpoint da API) não deve ser alterado, somente quando _when_ for ativado.
