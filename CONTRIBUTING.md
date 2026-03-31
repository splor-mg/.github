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
- [Padrões de Código](#padrões-de-código)
- [Dúvidas e Suporte](#dúvidas-e-suporte)

---

## Pré-requisitos

Antes de iniciar qualquer contribuição:

- Certifique-se de ter acesso ao repositório e às ferramentas necessárias
- Configure seu ambiente de desenvolvimento conforme o `README.md` do projeto
- Verifique se não há trabalho em andamento relacionado ao que você pretende fazer
- Visite o nosso post sobre [Setup da máquina](https://splor-mg.github.io/handbook/blog/setup-da-m%C3%A1quina/)
---

## Fluxo de trabalho
```
Issue → Branch → Desenvolvimento → Pull Request → Revisão → Merge
```

1. Toda contribuição deve ter um **issue associado** antes de ser iniciada
2. Crie uma **branch** a partir de `main` seguindo a nomenclatura definida
3. Desenvolva com **commits atômicos e descritivos**
4. Abra um **Pull Request** referenciando o issue
5. Aguarde **revisão e aprovação** antes do merge

---

## Abrindo Issues

Issues são o ponto de entrada de toda alteração, seja correção de bug, nova
funcionalidade ou melhoria. Um issue bem descrito reduz retrabalho e facilita a
priorização pela equipe.

### Antes de abrir

- Pesquise nos issues existentes para evitar duplicatas
- Para vulnerabilidades ou informações sensíveis, **não abra um issue público** —
  comunique diretamente o(a) responsável.

### Título

O título deve ser claro, específico e orientado à ação.

| | Exemplo |
|---|---|
| ❌ **Incorreto** | `bug no sistema` |
| ✅ **Correto** | `[BUG] Falha na validação de CPF no formulário de cadastro` |

| | Exemplo |
|---|---|
| ❌ **Incorreto** | `melhorar relatório` |
| ✅ **Correto** | `[FEAT] Adicionar filtro por período no relatório de produtividade` |

### Corpo do issue

Um issue bem estruturado deve conter:

**Para bugs:**
- Descrição objetiva do problema
- Passos para reproduzir
- Comportamento esperado vs. comportamento observado
- Ambiente (sistema operacional, versão, etc.)
- Evidências: logs, capturas de tela ou trechos de código relevantes

**Para funcionalidades ou melhorias:**
- Contexto e justificativa da necessidade
- Descrição do comportamento esperado
- Critérios de aceite objetivos e verificáveis

---

## Padrão de Commits

Adotamos o padrão [Conventional Commits](https://www.conventionalcommits.org/) para
garantir histórico legível e geração automatizada de changelogs.

### Estrutura
```
<tipo>(<escopo>): <descrição no imperativo>

[corpo opcional — o quê e por quê, não o como]

[rodapé opcional — referências, breaking changes]
```

### Tipos

| Tipo | Uso |
|---|---|
| `feat` | Nova funcionalidade |
| `fix` | Correção de bug |
| `docs` | Alterações em documentação |
| `refactor` | Refatoração sem mudança de comportamento |
| `test` | Adição ou correção de testes |
| `chore` | Tarefas de manutenção, configuração, dependências |
| `style` | Formatação sem impacto funcional |

### Exemplos

| | Exemplo |
|---|---|
| ❌ **Incorreto** | `git commit -m "ajustes"` |
| ✅ **Correto** | `git commit -m "fix(auth): corrige expiração incorreta do token JWT"` |

| | Exemplo |
|---|---|
| ❌ **Incorreto** | `git commit -m "wip"` |
| ✅ **Correto** | `git commit -m "feat(relatorio): adiciona filtro por período na exportação"` |

### Boas práticas

- Um commit deve representar **uma única mudança lógica**
- A descrição deve estar no **imperativo** ("adiciona", "corrige", "remove")
- Evite commits de "trabalho em progresso" — ajuste o histórico com `rebase`
  antes de abrir o PR
- Referencie o issue no rodapé quando aplicável: `Closes #42`

---

## Pull Requests

### Nomenclatura da branch
```
<tipo>/issue-<número>-<descricao-curta>

feat/issue-42-filtro-relatorio
fix/issue-17-validacao-cpf
docs/issue-8-guia-instalacao
```

### Criando o PR

- Preencha o template disponível ao abrir o PR
- Referencie o issue com `Closes #<número>` para fechamento automático
- Marque como **Draft** enquanto o trabalho estiver em andamento
- Solicite revisão somente quando o PR estiver pronto para merge

### Checklist antes de solicitar revisão

- [ ] O código compila e todos os testes passam localmente
- [ ] Foram adicionados testes para as mudanças realizadas
- [ ] A documentação foi atualizada, se necessário
- [ ] Os commits seguem o padrão definido
- [ ] O PR está associado a um issue

### Tamanho dos PRs

Prefira PRs pequenos e focados. PRs com mais de 400 linhas alteradas dificultam a
revisão e aumentam o risco de regressões. Se necessário, divida em PRs menores e
sequenciais.

---

## Revisão de Código

### Para quem revisa

- Priorize a revisão de PRs abertos antes de iniciar novo desenvolvimento
- Seja objetivo e construtivo — aponte o problema e, quando possível, sugira a solução
- Distingua entre bloqueantes (impedem o merge) e sugestões (melhorias opcionais)

### Para quem recebe a revisão

- Responda a todos os comentários antes de solicitar nova revisão
- Não faça force push após a revisão ter sido iniciada sem comunicar o revisor
- Em caso de discordância técnica, abra uma discussão — a decisão final cabe ao
  responsável técnico do projeto

---

## Padrões de Código

Cada repositório pode ter configurações específicas de linter e formatter. Consulte
o `README.md` do projeto. 

---

## Dúvidas e Suporte

- Dúvidas técnicas sobre o projeto: consulte a documentação em `docs/` ou o
  `README.md`
-  Abra um Issue no repositório ou consulte as informações da [SPLOR](https://www.mg.gov.br/planejamento/pagina/geral/quem-e-quem#subsecretaria-de-planejamento-e-orcamento) e, se possível, envie sua mensagem via Microsoft Teams.