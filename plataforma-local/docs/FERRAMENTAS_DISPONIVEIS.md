# Ferramentas disponíveis (verificado em 2026-10-29)

Cada item abaixo foi checado por comando ou consulta. O que não foi confirmado está marcado.

## Ambiente

- Workspace Linux na nuvem da Anthropic, pasta `/home/claude`. Não é o computador do dono e
  não está conectado ao VS Code dele.
- `/home/claude` não era um repositório git e não continha nenhum projeto (nem o site atual).
- Plano gratuito: sem tarefas agendadas, sem controle de navegador, sem controle do computador.

## Runtimes e CLIs

| Item | Resultado |
|---|---|
| Node | v22.23.4 |
| npm / pnpm / yarn | 10.9.9 / 10.28.0 / 1.22.22 |
| Python / pip | 3.13.18 / 26.2.1 |
| git | 2.43.0 |
| gh (GitHub CLI) | 2.89.0, mas **token inválido** (`GH_TOKEN`) |
| docker (CLI) | 29.9.2, mas **daemon indisponível** (sem `/var/run/docker.sock`) |
| psql | 16.15 (somente cliente; nenhum servidor PostgreSQL verificado) |
| Não encontrados | sqlite3, supabase, firebase, vercel, netlify |

## GitHub

- `list_repos` retornou lista vazia: nenhum repositório está acessível a esta sessão.
- Consequências: não é possível criar o repositório novo no GitHub a partir daqui, e também
  não há acesso ao repositório do site atual (o que protege o site).

## Conectores

- Context7 (documentação de bibliotecas): conectado e habilitado nesta sessão.
- Nenhum conector de banco de dados, hospedagem, GitHub, mapas ou e-mail.

## Plugins habilitados na conta

TypeScript/JavaScript LSP, superpowers (TDD, depuração, planos), code-review, feature-dev,
frontend-design, revisão de segurança, Playwright MCP, Context7.
Observação: as ferramentas do Playwright MCP **não aparecem carregadas nesta sessão**, então
não foi confirmado que testes de navegador possam ser executados por esse caminho.

## Rede

- Há proxy de saída. `registry.npmjs.org` falhou com `ENOTFOUND` em duas tentativas
  (`npm view`). **Neste momento não é possível instalar pacotes npm.** Retestar em cada sessão.
- Navegadores do Playwright não estão instalados.

## Credenciais presentes no ambiente

Variáveis como `GH_TOKEN` pertencem à sessão do Claude, não ao projeto. Não devem ser usadas
nem copiadas para esta plataforma.
