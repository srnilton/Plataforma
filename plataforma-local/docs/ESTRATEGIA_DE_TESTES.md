# Estratégia de testes automatizados

Os nomes de ferramentas abaixo são sugestões para uma stack TypeScript. Serão confirmados
quando a stack for decidida (ver `STATUS_DO_PROJETO.md`).

## Camadas

1. **Unitários** (maioria): regras de negócio puras, como cálculo de nota média, regras de
   pontos, validação de entrada e normalização de busca. Rápidos, sem rede nem banco.
   Sugestão: Vitest.
2. **Integração**: API/serviços contra um banco de teste descartável (PostgreSQL), incluindo
   migrações, permissões e consultas de busca.
3. **Ponta a ponta (E2E)**: poucos fluxos críticos no navegador (cadastro, login, buscar
   local, avaliar, ver pontos). Sugestão: Playwright.
4. **Segurança**: testes dedicados a XSS, autorização (usuário A não altera dados do B),
   limites de taxa e fraude de pontos. Dependências auditadas (`npm audit` ou equivalente).
5. **Acessibilidade**: verificação automatizada nas telas principais.

## Regras

- Desenvolvimento orientado a testes: teste que falha primeiro, depois a implementação.
- Dados de teste sempre sintéticos. Banco de teste separado. Nunca dados reais nem de produção.
- Serviços externos (mapas, e-mail, login social) são simulados nos testes. Testes que
  chamam serviço real ficam em suíte à parte, opcional e com credenciais próprias.
- Cada item do "Review Focus" do plano da V1 tem um teste nomeado.
- Cobertura mínima será definida junto com a stack. Cobertura não substitui os testes de
  fraude e de segurança.
- Integração contínua (GitHub Actions) só será criada no repositório NOVO, quando existir.
  Os pipelines nunca fazem deploy automático.

## O que pode ser executado hoje (2026-10-29)

| Camada | Situação | Motivo |
|---|---|---|
| Unitários | **Limitado** | Node 22 e pnpm presentes, mas a instalação de pacotes falha (npm `ENOTFOUND` em duas tentativas); só roda o que não depende de pacotes externos |
| Integração com banco | **Não possível agora** | Docker sem daemon; só há cliente `psql`, sem servidor confirmado |
| E2E | **Não possível agora** | Navegadores do Playwright não instalados; ferramentas do Playwright MCP não carregadas |
| Segurança / acessibilidade | Dependem das camadas acima | |

Nenhum teste existe ainda, porque ainda não há código.
