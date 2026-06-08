# Guia de Contribuição

Este documento estabelece os padrões e processos para contribuições nos repositórios internos da equipe. O cumprimento dessas diretrizes garante rastreabilidade, qualidade e consistência ao longo do ciclo de desenvolvimento.

Caso queira começar a contribuir e não saiba por onde iniciar, acesse o curso [Trilha-Dev](https://trilhadev.planejamento.mg.gov.br/main/).

## Sumário

- [Pré-requisitos](#pré-requisitos)
- [Fluxo de trabalho](#fluxo-de-trabalho)
- [Abrindo Issues](#abrindo-issues)
- [Padrão de Commits](#padrão-de-commits)
- [Pull Requests](#pull-requests)
- [Revisão de Código](#revisão-de-código)
---

## Pré-requisitos

Antes de iniciar qualquer contribuição, certifique-se de ter as ferramentas
necessárias para o tipo de participação desejada:

- **Issues e discussões** — basta ter uma conta no GitHub.
- **Pull requests e revisões de código** — requer acesso ao repositório e ambiente
  configurado conforme o `README.md` do projeto.


## Fluxo de trabalho
Issue → Branch → Desenvolvimento → Pull Request → Revisão → Merge

1. Toda contribuição começa com um **issue associado**.
2. Crie uma **branch** a partir de `main` seguindo a nomenclatura definida.
3. Desenvolva com **commits atômicos e descritivos**.
4. Abra um **Pull Request** referenciando o issue.
5. Aguarde **revisão e aprovação** antes do merge.


## Abrindo Issues

- Pesquise nos issues existentes para evitar duplicatas.
- Para vulnerabilidades ou informações sensíveis, **não abra um issue público** —
  comunique diretamente o responsável.
- O título deve ser claro e orientado à ação:
  - ❌ `bug no sistema`.
  - ✅ `[BUG] Erro 500 ao tentar exportar relatório em PDF`.


## Padrão de Commits

Adotamos o padrão [Conventional Commits](https://www.conventionalcommits.org/).
<tipo>(<escopo>): <descrição no imperativo>

| Tipo       | Uso                                        |
|------------|--------------------------------------------|
| `feat`     | Nova funcionalidade                        |
| `fix`      | Correção de bug                            |
| `docs`     | Alterações em documentação                 |
| `refactor` | Refatoração sem mudança de comportamento   |
| `test`     | Adição ou correção de testes               |
| `chore`    | Manutenção, configuração, dependências     |

- A descrição deve estar no **imperativo** ("adiciona", "corrige", "remove").
- Um commit deve representar **uma única mudança lógica**.
- Referencie o issue no rodapé quando aplicável: `Closes #42`.

## Pull Requests

Nomenclatura da branch:
<tipo>/issue-<número>-<descricao-curta>

- Referencie o issue com `Closes #<número>` para fechamento automático.
- Marque como **Draft** enquanto o trabalho estiver em andamento.
- Prefira PRs pequenos e focados — PRs com muitas linhas dificultam a revisão.


## Revisão de Código

**Para quem revisa:**

- Seja objetivo e construtivo — aponte o problema e sugira a solução quando possível.
- Distingua entre bloqueantes e sugestões opcionais.

**Para quem recebe a revisão:**

- Responda a todos os comentários antes de solicitar nova revisão.
- Em caso de discordância técnica, abra uma discussão — a decisão final cabe ao
  responsável técnico do projeto.


## Dúvidas e Suporte

- Dúvidas técnicas sobre o projeto: consulte a documentação em `docs/` ou o
  `README.md`.
-  Abra um Issue no repositório ou consulte as informações da [SPLOR](https://www.mg.gov.br/planejamento/pagina/geral/quem-e-quem#subsecretaria-de-planejamento-e-orcamento) e, se possível, envie sua mensagem via Microsoft Teams.
