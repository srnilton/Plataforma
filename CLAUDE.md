# CLAUDE.md — Plataforma de descoberta local, comunidade, avaliações e recompensas

Regras permanentes deste projeto. Leia antes de qualquer tarefa.

## 0. Regra suprema: preservar o site atual do dono

O dono tem um site já publicado e funcionando, com repositório, hospedagem e backend próprios.
**Este projeto é totalmente independente dele.** A preservação do site atual tem prioridade
sobre qualquer tarefa de desenvolvimento.

Proibido, sem autorização explícita do dono:

1. Abrir, modificar, excluir, substituir ou reorganizar arquivos do site atual.
2. Fazer commit, push, merge ou qualquer alteração no repositório do site atual.
3. Alterar hospedagem, domínio, DNS, backend, banco de dados, variáveis de ambiente ou
   pipelines de implantação do site atual.
4. Publicar qualquer coisa automaticamente (deploy, release, push para produção).
5. Conectar este projeto à hospedagem ou ao domínio existentes.
6. Reutilizar credenciais, bancos de dados ou serviços de produção do site atual.
7. Executar comandos destrutivos ou que possam afetar outros projetos.

Se uma tarefa exigir acesso ao site atual: interromper essa tarefa, explicar o motivo e
aguardar autorização.

## 1. Verificação no início de cada sessão

Antes de alterar qualquer arquivo, rodar `pwd`, `git rev-parse --show-toplevel` e
`git remote -v`. Só prosseguir se a pasta for a raiz deste projeto e o remote (quando existir)
for o repositório NOVO desta plataforma. Se não for possível confirmar, parar e pedir
autorização.

## 2. O projeto

- Plataforma de descoberta local, comunidade, avaliações e recompensas.
- Pasta: `plataforma-local/` (nome provisório).
- Repositório GitHub: `srnilton/Plataforma`, confirmado como o repositório novo desta
  plataforma. Nenhum outro repositório do dono deve ser aberto ou alterado.
- Ordem de trabalho definida pelo dono: primeiro rodar localmente; nuvem e provedores só
  depois, com autorização.
- Especificação do produto: `docs/superpowers/specs/2026-10-29-especificacao-do-produto.md`.
  É a fonte de verdade do escopo.
- Stack: candidata na especificação, proposta em `docs/ARQUITETURA_RECOMENDADA.md`, ainda
  não aprovada.
- Escopo atual: somente a Versão 1, conforme `docs/superpowers/plans/2026-10-29-versao-1.md`.
  Não antecipar as Atualizações 1 a 5.

## 3. Convenções

- Documentação e textos de interface em pt-BR.
- Segredos nunca entram no repositório. `.env` é ignorado pelo git; `.env.example` contém
  apenas nomes de variáveis, sem valores.
- Credenciais, banco e serviços exclusivos desta plataforma. Lista em
  `docs/CREDENCIAIS_E_INTEGRACOES.md`.
- Desenvolvimento orientado a testes. Nada é dado como concluído sem rodar os testes e
  conferir a saída (ver `docs/ESTRATEGIA_DE_TESTES.md`).
- Não declarar uma ferramenta ou integração como conectada sem verificar. O que foi
  verificado fica em `docs/FERRAMENTAS_DISPONIVEIS.md`.
- Commits pequenos e focados, só neste repositório.
- Dados pessoais (LGPD): coletar o mínimo, pedir consentimento e prever exclusão de conta.
- Ao fim de cada sessão, atualizar `docs/STATUS_DO_PROJETO.md` com o estado real.

## 4. Documentação

Índice em `docs/README.md`.
