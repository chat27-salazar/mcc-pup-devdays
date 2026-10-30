<!-- l10n-sync: source-file="04-design-vibes.md" -->
# Parte 4: Tema Orientado a Design

---

Nesta parte, você vai usar o **Plan Mode** para projetar uma transformação visual completa e o **Agent Mode** para implementá-la. Isso é desenvolvimento orientado a design — comece com a visão, itere nos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Insira este prompt:

> Quero transformar esta página em uma experiência completa de arcade retrô. Planeje uma reformulação visual abrangente que inclua: efeitos de linhas de varredura CRT no fundo, brilho neon no título pulsando como um letreiro, selo VS animado com mudanças de cor no gradiente, sobreposição de brilho e cintilação nos cartões de resultados, animações de entrada flutuante nos campos de texto, texto de carregamento alternando entre verde e roxo e efeitos de brilho ao passar o cursor sobre os quadrados de contribuição. Mantenha o fundo escuro (#0a0a1a) com detalhes em verde (#5fed83) e roxo (#8a2be2). Use um tema escuro com a fonte retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano de implementação detalhado cobrindo todos os efeitos visuais. **Não aceite imediatamente** — revise o plano e itere:

- Sugira ajustes no tempo das animações (por exemplo, "Deixe a pulsação do neon mais lenta, em torno de 3 segundos").
- Pergunte sobre efeitos específicos (por exemplo, "Como a sobreposição cintilante vai funcionar nos cartões?").
- Solicite mudanças na abordagem se algo não parecer correto

<!-- track:vscode:start -->
Quando estiver satisfeito com o plano, mude para o modo **Agent** e peça ao Copilot para implementá-lo.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Quando estiver satisfeito com o plano, peça ao Copilot CLI para implementá-lo.
<!-- track:cli:end -->

## Tarefa 2: Implemente o Tema

> Implemente o plano do tema de arcade retrô que acabamos de criar.

O Copilot vai adicionar múltiplas animações CSS, pseudo-elementos e transições na sua folha de estilos. Isso pode incluir:

- `@keyframes` para scanlines, pulso neon, shimmer e efeitos de float-in
- Pseudo-elementos (`::before`, `::after`) para efeitos de sobreposição
- CSS custom properties para as cores do tema
- Estados de transição e hover para elementos interativos

<!-- track:cli:start -->
Quando as alterações forem concluídas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Refine o estilo visual

> **⚠️ Não está vendo as mudanças?** Se o novo tema ou as animações não aparecerem, pare o servidor (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador forçando a recarga (`Ctrl+Shift+R`).

Mantenha a pré-visualização do navegador aberta e itere no design. Experimente instruções como:

> O efeito de linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma leve oscilação elétrica ao texto do título.

> O selo VS deve pulsar com mais intensidade.

Isso é **desenvolvimento orientado a design**: você itera no resultado visual em tempo real. Cada instrução aprimora a experiência até chegar ao resultado desejado. Não se contente com "bom o suficiente" — refine o estilo até a página parecer saída de um fliperama.

## Tarefa 4: Atualize as Instruções

Suas instruções devem refletir as decisões importantes de design. Peça ao Copilot:

<!-- track:vscode:start -->
> Adicione uma seção de guia de design a copilot-instructions.md descrevendo nosso tema de arcade retrô: cores, fontes e estilo das animações.
<!-- track:vscode:end -->

<!-- track:cli:start -->
> Atualize as instruções do repositório com um guia de design curto para o tema de arcade retrô: cores, fontes, estilo das animações e a regra de que a nova interface deve manter a estética neon.
<!-- track:cli:end -->

Isso mantém futuras interações com o Copilot consistentes com a identidade visual que você estabeleceu. Qualquer nova funcionalidade ou componente seguirá automaticamente a estética retrô arcade.

Faça commit das instruções atualizadas e das alterações de design quando a página estiver como você quer.

## ✅ Parte 4 Concluída

**O que você aprendeu:**

- **Plan Mode para sistemas de design** — esboce uma reformulação visual completa antes de escrever qualquer código
- **Iterar na saída visual** — use prompts rápidos de acompanhamento para ajustar animações, cores e efeitos
- **Manter as instruções atualizadas com decisões de design** — documente seu tema para que o Copilot mantenha a consistência
- **Fluxo de desenvolvimento orientado a design** — comece com a visão, implemente com IA, refine até ficar perfeito
