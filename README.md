# Proway-projeto-git

Projeto para demonstrar e praticar fluxos de trabalho do GitHub (branching, pull requests, CI/CD) seguindo práticas similares ao Git Flow.

## Sumário
- [Visão Geral](#visão-geral)  
- [Recursos](#recursos)  
- [Pré-requisitos](#pré-requisitos)  
- [Fluxo de Branches](#fluxo-de-branches)  
- [Integração Contínua (CI)](#integração-contínua-ci)  
- [Contribuindo](#contribuindo)  

## Visão Geral
Repositório de exemplo focado em ensinar e aplicar:
- Convenções de branches (feature, develop, release, hotfix, main).
- Boas práticas de commits e mensagens.
- Automação de testes e deploy via GitHub Actions.
- Criação automática de tag pelo GitHub Actions.

## Recursos
- Estrutura de branches padronizada.
- Templates para Pull Request e Issue (sugestão).
- Exemplo de workflow de CI (build/test) no GitHub Actions.
- Guia de contribuição simples.

## Pré-requisitos
- Git
- Ferramentas do projeto (por exemplo, Python, Docker)

## Fluxo de Branches
- main: versão estável, deployable.
- develop: integração de features, preparação para release.
- feature/<nome>: desenvolvimento de funcionalidades.
- release/<versão>: preparação para release (correções menores, docs).
- hotfix/<nome>: correções críticas em produção.

Recomenda-se criar PRs da branch feature para develop e de release/hotfix para main e develop conforme necessário.

## Integração Contínua (CI)
- Configurar workflows no diretório .github/workflows:
  - build.yml: build e testes em pushes e PRs.
  - lint.yml: verificação de estilo/codificação.
  - release.yml (opcional): deploy automatizado ao criar uma tag / merge para main.
- Garantir que o CI execute em múltiplas versões/ambientes quando aplicável.

## Contribuindo
1. Fork do repositório.
2. Criar branch feature/<descrição>.
3. Fazer commits pequenos e com mensagens claras (ex: feat: adicionar validação de email).
4. Abrir PR para develop com descrições e passos para reproduzir/testar.
5. Corrigir feedbacks dos revisores.