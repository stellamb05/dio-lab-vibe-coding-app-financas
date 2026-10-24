# Entrega do Desafio: App de Finanças Pessoais "Pé no Chão" com Vibe Coding

**Acesse o MVP rodando ao vivo aqui:** [Testar o App Pé no Chão](https://saldo-em-equili.lovable.app)

**Projeto:** App Pé no Chão (Vibe Coding)  
**Aluna / PO / QA:** Stella Mendes Batista  
**Bootcamp:** DIO / Santander - App com IA  
**Data:** Outubro de 2026

## 1. Resumo do App de Finanças Pessoais
O **"Pé no Chão"** é um aplicativo financeiro (MVP) desenvolvido com a abordagem de *Vibe Coding*. Seu objetivo é eliminar a barreira das planilhas complexas e da estética fria dos bancos tradicionais. O app permite que o usuário registre sua vida financeira através de conversas naturais ou áudio (Speech-to-Text) com a assistente virtual "Tutu", que possui uma personalidade empática e brasileira. Ele processa colagens diretas de faturas e SMS, categoriza os gastos automaticamente e gera painéis visuais simples (como o Gráfico de Rosca), além de permitir o controle de "Metas" (cofrinhos) e status de pagamento através de um sistema de "Check" (✓) inspirado em cadernos físicos.

## 2. Prompt Final (PRD Consolidado v5.0)
*Este foi o escopo técnico final (Product Requirements Document) injetado no Lovable para gerar o aplicativo completo, englobando todas as iterações e refinamentos.*

```markdown

# Super Atualização de PRD: Responsividade Global Multi-Dispositivo, 5 Abas e Filtro Inteligente

## 1. Responsividade Global e Adaptabilidade Multi-Dispositivo (TODO O APP)
A adaptação de tamanho, fontes, margens e layout DEVE ser aplicada a TODAS as abas e componentes do aplicativo de forma 100% automática e fluida conforme o dispositivo detectado (breakpoints do Tailwind CSS):
- Versão Computador (Desktop): Layout expansivo em múltiplas colunas equilibradas, aproveitando a largura da tela com excelente espaçamento e legibilidade.
- Versão Tablet: Disposição intermediária responsiva em 2 colunas, com elementos touch-friendly.
- Versão Celular (Mobile - Todas as Abas): 
  - Conversa: O chat da Tutu e o campo de digitação/áudio devem ocupar a tela sem criar rolagem dupla ou quebrar caixas de texto.
  - Histórico: Tabela/lista de transações adaptada para telas estreitas.
  - Metas: Os cards de metas devem se ajustar para ocupar a largura da tela sem estourar margens.
  - Painel: Os 3 cards de resumo superiores ("Saldo", "Entrou", "Saiu") devem usar uma grelha ultra-compacta ou carrossel horizontal. O Gráfico de Rosca DEVE estar visível imediatamente ao abrir a aba, sem exigir rolagem.
  - Visão Geral: Componentes empilhados sem rolagem desnecessária.

## 2. Nome Oficial, Cadastro Completo e LGPD
- Nome: O aplicativo se chama "Pé no Chão" (com acentuação correta em toda a interface).
- Cadastro: O formulário de registro inicial DEVE exigir obrigatoriamente: Nome Completo, Data de Nascimento, E-mail e Senha.
- LGPD: Checkbox obrigatório de aceite dos Termos de Uso e Privacidade na criação da conta.

## 3. Reestruturação do Menu em 5 Abas Independentes
O menu de navegação deve ter exatamente 5 abas com isolamento estrito de componentes:
1. Conversa: Chat da Tutu ("Seu bloco de notas inteligente") com suporte a áudio (Speech-to-Text via microfone) e leitor inteligente de notificações de banco/SMS (perguntando como o usuário deseja renomear o nome fantasia do estabelecimento). O chat deve iniciar limpo ao abrir, sem histórico longo ou lista de registros antigos abaixo dele.
2. Histórico: NOVA ABA exclusiva para listar todas as transações de entradas e saídas. Deve conter ícone de lápis para edição e botão interativo de Check (✓) para alternar o status entre pago/recebido (Verde Menta) e pendente (Cinza).
3. Metas: Aba exclusiva para a exibição e criação dos cards de "Minhas Metas", com modal de edição para alterar o Nome da Meta e o Valor Alvo.
4. Painel: Visão macro contendo apenas os cards compactos de resumo e o Gráfico de Rosca (Donut Chart) centralizado com o "TOTAL GASTO: R$ [Valor]" no centro. REMOVA a lista de registros consolidados do final desta tela.
5. Visão Geral: Análise detalhada com o "Resumo Financeiro Unificado" (Balanço + Saldo combinados num único card de destaque) e controles de sub-abas internas ("Despesas" e "Receitas") para alternar as barras de categorias sem poluição visual.

## 4. Único Dropdown Inteligente de Período
Substitua múltiplos seletores por um Único Dropdown Inteligente de Período no topo das abas Painel e Visão Geral (ex: "Outubro de 2026", "Último Trimestre", "Ano Atual"). Ao selecionar uma opção, todos os gráficos e indicadores da tela são recalculados automaticamente.

## Entregável
Garanta responsividade automática em todo o aplicativo (Desktop, Tablet e Mobile) em todas as 5 abas. Aplique a tela de cadastro completa com Data de Nascimento e LGPD, mova a lista de transações para o "Histórico", mantenha o chat da Tutu limpo, adicione o gráfico de rosca no Painel e refatore a Visão Geral com o Balanço unificado e sub-abas.
```

## 3. Imagens da Interface (Evidências)
*(Arraste as imagens do Lovable para baixo desta linha)*

*   <img width="886" height="498" alt="image" src="https://github.com/user-attachments/assets/cd522f17-ee95-4340-a2df-0e29cfd0211a" />

*   <img width="886" height="498" alt="image" src="https://github.com/user-attachments/assets/b5802d56-a027-4de9-ab4f-e8d3ed7305ac" />

*   <img width="886" height="498" alt="image" src="https://github.com/user-attachments/assets/f43abf4b-9efd-4393-a203-bf6d0c14a403" />

*   <img width="886" height="498" alt="image" src="https://github.com/user-attachments/assets/31380fc6-ff9d-4401-b3b9-183ae07cc3e3" />


## 4. Reflexão sobre o Processo

### O que funcionou bem?
A estruturação prévia das regras de negócio através de um Product Requirements Document (PRD) rigoroso. Atuar com uma visão de Product Owner (PO) me permitiu definir a arquitetura e a identidade visual (Design Universal, paleta pop inspirada em canetas) antes mesmo de gerar a primeira tela. Além disso, a estratégia de testar e refinar os prompts em LLMs gratuitos (como Copilot e Gemini) antes de injetá-los no Lovable funcionou perfeitamente para economizar os créditos de compilação da ferramenta.

### O que não funcionou como o esperado?
O limite restrito de 5 interações diárias no plano gratuito do Lovable exigiu pausas forçadas no desenvolvimento, obrigando a um planeamento rigoroso. Além disso, a IA do Lovable teve dificuldade inicial com a gestão de estado do React, gerando "ilhas" de código (onde o chat não conseguia atualizar os cofrinhos) e criando poluição visual (como filtros duplicados e scroll excessivo no mobile).

### O que aprendeu sobre conversar com IAs?
Aprendi que *Vibe Coding* não é apenas pedir para a IA "fazer uma app", mas sim guiá-la de forma técnica e objetiva. A IA responde excecionalmente bem quando atuamos como Analistas de QA (Quality Assurance), apontando erros específicos na interface, exigindo o isolamento estrito de componentes em abas e ditando regras claras de UX/UI (como a unificação de elementos e responsividade via `Tailwind CSS`). No Vibe Coding, a precisão da linguagem determina a usabilidade final do produto.
