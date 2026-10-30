# Arquitetura recomendada (proposta — aguardando aprovação do dono)

Segue a seção 4 da especificação. Nada abaixo foi instalado. Versões de bibliotecas **não
foram verificadas** (sem acesso ao registro npm nesta sessão); devem ser confirmadas na
documentação oficial antes de adotar.

## Visão geral

SPA em React consumindo uma API REST versionada (`/v1`), com PostgreSQL. Frontend e backend
em repositório único (monorepo) para simplificar testes e versionamento.

## Decisões

| Tema | Recomendação | Vantagens | Desvantagens | Muda custo/privacidade/escopo? |
|---|---|---|---|---|
| Frontend | React + TypeScript + Vite + Tailwind | Ecossistema grande, build rápido, bem adotado | Sem renderização no servidor: SEO das páginas públicas é limitado | Não |
| SEO das páginas de locais | Avaliar pré-renderização ou SSR na Fase 3 | Páginas públicas encontráveis em buscadores | Mais complexidade de hospedagem | **Sim, decidir antes da Fase 3** |
| Backend | NestJS | Módulos, injeção de dependências e guards ajudam a separar autorização e regras de negócio num produto grande | Mais código inicial e curva de aprendizado | Não |
| Alternativa de backend | Fastify puro | Mais leve e simples | Organização depende de disciplina da equipe | Não |
| Banco | PostgreSQL; PostGIS se a busca por proximidade exigir | Integridade, transações e consultas geográficas | PostGIS precisa estar disponível no provedor escolhido | **Sim (custo/provedor)** |
| ORM | Decidir entre Prisma e Drizzle na Fase 0, após ler a documentação oficial de PostGIS em cada um | Prisma: migrações e DX; Drizzle: mais controle de SQL | Suporte geográfico pode exigir SQL manual | Não |
| Autenticação | Sessão em cookie HttpOnly/Secure/SameSite, hash de senha Argon2id, biblioteca mantida (sem criptografia caseira) | Cookies HttpOnly reduzem risco de roubo por XSS | Frontend e API em domínios diferentes exigem configuração cuidadosa | Não |
| Autorização | Papéis e permissões validados no servidor em todo endpoint | Atende a regra de que o ID enviado não dá acesso | Exige testes sistemáticos por endpoint | Não |
| Validação | Zod no frontend e no backend (esquemas compartilhados no monorepo) | Uma fonte de regras | Acoplamento entre pacotes | Não |
| Mapas | Biblioteca de mapas open source com provedor de tiles de custo previsível | Evita dependência de preço por carregamento | Qualidade e limites variam por provedor; servidores públicos do OpenStreetMap e do Nominatim têm política de uso que não serve para produção com tráfego | **Sim (custo e licença), comparar provedores antes de decidir** |
| Redis | Não usar na V1 | Menos infraestrutura | Rate limiting fica em memória/banco, suficiente para um só servidor | Não |
| Hospedagem | Frontend na Hostinger (estático) e API no Render, conforme a especificação; banco gerenciado | Alinhado com o que o dono já usa | Domínios diferentes; confirmar se a Hostinger do dono serve SPA com rotas | **Sim (custo)**; nunca reutilizar a conta/domínio do site atual sem autorização |
| Ambientes | desenvolvimento, homologação, produção, com credenciais separadas | Isolamento | Custo de manter três | Não |

## Pontos de atenção

- Domínio: se o frontend e a API ficarem em subdomínios do mesmo domínio, os cookies de
  sessão funcionam melhor. **Isso exige mexer em DNS, o que só será feito com autorização
  explícita e nunca no domínio do site atual.**
- Imagens de usuário não entram na V1, a menos que o dono decida o contrário (traz custo,
  moderação e privacidade).
- Dados de estabelecimentos: só de fontes cuja licença permita o uso (spec, seção 7).
- Registrar cada decisão aprovada na seção "Decisões" do `STATUS_DO_PROJETO.md`.

## Primeiro rodar localmente (decisão do dono)

Hospedagem, banco gerenciado e domínio ficam para depois. Para desenvolver só no computador
do dono, nada depende de conta em nuvem:

- **Banco:** PostgreSQL local (instalado ou em contêiner). Banco separado para testes.
- **E-mails** (confirmação, recuperação de senha): ferramenta que captura e-mails localmente,
  como o Mailpit, em vez de provedor real.
- **Variáveis de ambiente:** arquivo `.env` local, ignorado pelo git, com valores próprios
  deste projeto.
- **Mapas:** continua pendente. Em desenvolvimento leve é possível usar um provedor de tiles
  de teste; a escolha definitiva (custo e licença) fica para antes da publicação.
- **Cookies e CORS:** frontend e API rodam em portas diferentes de `localhost`; a configuração
  de sessão local precisa ser documentada junto, para não surpreender na publicação.
- **Pré-requisitos no computador:** Node.js LTS, gerenciador de pacotes, PostgreSQL ou
  Docker, git. Será informado o que falta conforme o que o dono tiver.
