# Status do projeto

**Última atualização:** 2026-10-29 (noite)

## Resumo

Fase de preparação. **Não existe código.** Há regras permanentes, documentação, a
especificação do produto, uma arquitetura proposta e o plano da Versão 1. Decisão do dono:
**primeiro fazer o sistema rodar localmente; nuvem e provedores ficam para depois.**

## Repositório e pasta

- Repositório no GitHub: `srnilton/Plataforma`. **Confirmado como o repositório novo**: tem
  um único commit do dono (`0a985ba`, "inicializando projeto plataforma-local") com os 10
  arquivos de preparação, sem segredos e sem arquivos do site atual.
- Os arquivos estão dentro de uma subpasta `plataforma-local/` no repositório, não na raiz.
  Decidir se mantém assim ou se move para a raiz.
- O repositório recebeu depois apenas o que está neste commit; a especificação, a arquitetura
  e o plano corrigido **ainda não estão nele**.
- **Envio (push) pela sessão do Claude foi recusado**: falta instalar o aplicativo Claude
  no GitHub para esse repositório. Até lá, os arquivos novos chegam por zip, copiados pelo
  dono.
- Visibilidade: **pública** no momento da verificação. O dono pediu que seja privada; essa
  alteração precisa ser feita por ele no GitHub (a sessão não tem como mudar).
- Pasta de trabalho da sessão: `/home/claude/plataforma-local/` (git local, sem remote) e
  um clone de leitura em `/home/claude/plataforma/`.
- Hospedagem, domínio, banco e serviços: nada configurado nem conectado.

## Site atual do dono

Não foi acessado, aberto nem alterado. Não há pasta, repositório ou credencial dele neste
ambiente.

## Tecnologias e funcionalidades existentes

Nenhuma. Stack candidata em `ARQUITETURA_RECOMENDADA.md`.

## Arquivos do projeto

`CLAUDE.md`, `README.md`, `.gitignore`, `.env.example`, `docs/README.md`,
`docs/STATUS_DO_PROJETO.md`, `docs/FERRAMENTAS_DISPONIVEIS.md`,
`docs/ESTRATEGIA_DE_TESTES.md`, `docs/CREDENCIAIS_E_INTEGRACOES.md`,
`docs/ARQUITETURA_RECOMENDADA.md`,
`docs/superpowers/specs/2026-10-29-especificacao-do-produto.md`,
`docs/superpowers/plans/2026-10-29-versao-1.md`.

## Testes

Nenhum teste existe. O que dá para executar neste ambiente está em `ESTRATEGIA_DE_TESTES.md`.

## Decisões pendentes (do dono)

1. Tornar o repositório privado (ação do dono no GitHub).
2. Instalar o aplicativo Claude no GitHub para o repositório, ou continuar copiando por zip.
3. Onde fica o código: subpasta `plataforma-local/` ou raiz do repositório.
4. Onde desenvolver e rodar: o computador do dono é o caminho, pois este workspace não
   instala pacotes npm, não roda Docker nem testes de navegador. Precisamos saber o que o
   computador dele tem (sistema, Node, PostgreSQL ou Docker).
5. Aprovar ou ajustar `ARQUITETURA_RECOMENDADA.md`.
6. Nome provisório do produto.

## Correção registrada

A primeira versão do plano incluía pontos de recompensa na V1. A especificação do dono
coloca recompensas na Atualização 2; o plano foi corrigido.

## Próximos passos

1. Dono faz o repositório privado e informa o ambiente do computador dele.
2. Detalhar a Fase 0/1 em tarefas com testes, já para rodar localmente.
3. Começar a Fase 1 (fundação) onde os pacotes possam ser instalados.
