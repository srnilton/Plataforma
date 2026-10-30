# PROJETO: PLATAFORMA INTELIGENTE DE DESCOBERTA LOCAL, COMUNIDADE E RECOMPENSAS

## 1. SEU PAPEL

Você atuará como uma equipe multidisciplinar de desenvolvimento de software, composta por:

- Arquiteto de software sênior.
- Engenheiro full-stack.
- Especialista em React e desenvolvimento de interfaces modernas.
- Especialista em backend, APIs e bancos de dados.
- Engenheiro de segurança da informação.
- Especialista em inteligência artificial aplicada a negócios.
- Especialista em experiência do usuário (UX/UI).
- Engenheiro de infraestrutura, DevOps e integração contínua.
- Especialista em testes automatizados e qualidade de software.
- Especialista em prevenção a fraudes e proteção de dados.
- Product Manager responsável por organizar o produto em versões.

Sua missão é planejar, implementar, testar, documentar e preparar para publicação uma plataforma digital completa, escalável, moderna e comercialmente sustentável.

Não quero somente um protótipo visual, uma página estática ou um conjunto de telas sem funcionamento real.

Quero um produto de software funcional, com frontend, backend, banco de dados, autenticação, regras de negócio, segurança, testes e infraestrutura de implantação.

Não afirme que um recurso está concluído sem verificar sua implementação.

Não invente resultados de testes, integrações, credenciais, dados ou funcionalidades.

Se alguma etapa depender de uma conta externa, chave de API, pagamento, configuração ou autorização minha, implemente tudo o que for possível e informe exatamente o que preciso fornecer.

---

# 2. VISÃO DO PRODUTO

Desenvolva uma plataforma que una cinco grandes conceitos:

1. Descoberta de estabelecimentos e serviços locais.
2. Avaliações de consumidores com diferentes níveis de evidência.
3. Rede social e comunidade local.
4. Sistema de recompensas e campanhas promocionais.
5. Inteligência artificial para gerar informações úteis aos comerciantes.

O objetivo é criar um aplicativo que as pessoas tenham motivos reais para utilizar frequentemente.

O produto não deve ser apenas uma cópia do Google Maps, de uma rede social ou de um aplicativo de avaliações.

A inovação deverá estar na integração entre descoberta local, comunidade, experiências verificáveis, recompensas transparentes e inteligência comercial.

A plataforma começará conquistando consumidores e construindo uma comunidade ativa. Posteriormente, ampliará suas ferramentas comerciais para gerar receita recorrente.

O nome comercial ainda será definido. Portanto, utilize um nome provisório facilmente substituível e centralize as configurações de marca.

Toda a interface inicial deve estar em português brasileiro, com arquitetura preparada para futura internacionalização.

---

# 3. PRINCÍPIOS FUNDAMENTAIS

Siga estas regras durante todo o desenvolvimento:

1. Priorize um produto funcional, não apenas visualmente impressionante.
2. Desenvolva uma arquitetura organizada e de fácil manutenção.
3. Utilize versões estáveis e compatíveis das tecnologias escolhidas.
4. Consulte a documentação oficial das bibliotecas antes de adotar recursos importantes.
5. Não utilize bibliotecas abandonadas ou dependências desnecessárias.
6. Não coloque regras críticas de negócio somente no frontend.
7. Toda operação sensível deverá ser validada no backend.
8. Não armazene senhas em texto puro.
9. Não exponha chaves secretas no frontend ou no repositório.
10. Não utilize dados pessoais reais em testes automatizados.
11. Não simule integrações como se fossem reais.
12. Não utilize dados fictícios em produção sem identificá-los claramente.
13. Não permita manipulação comercial das avaliações.
14. Não recompense avaliações positivas especificamente.
15. Não implemente moeda negociável, criptomoeda ou transferência financeira sem avaliação jurídica e técnica apropriada.
16. Não exija rastreamento contínuo da localização dos usuários.
17. Implemente acessibilidade, privacidade e segurança desde o início.
18. Não acrescente funcionalidades complexas sem avaliar sua necessidade, custo e impacto.
19. Registre decisões técnicas importantes na documentação.
20. Mantenha o produto preparado para receber atualizações futuras.

Quando encontrar uma decisão técnica importante, apresente a opção recomendada, suas vantagens, suas desvantagens e os motivos da escolha.

Não interrompa todo o trabalho por causa de uma decisão secundária. Escolha uma alternativa razoável, documente-a e prossiga, solicitando minha aprovação quando a decisão alterar significativamente custos, privacidade, arquitetura ou escopo.

---

# 4. TECNOLOGIAS E ARQUITETURA

Antes de implementar, avalie as tecnologias estáveis mais adequadas ao projeto.

Considere preferencialmente:

## Frontend

- React.
- TypeScript.
- Vite.
- Tailwind CSS.
- Uma biblioteca acessível e mantida de componentes de interface.
- React Router ou solução equivalente de roteamento.
- TanStack Query ou ferramenta equivalente para gerenciamento de dados remotos.
- React Hook Form e Zod, ou alternativas equivalentes, para formulários e validação.
- Biblioteca de mapas compatível com o provedor escolhido.
- Testes com Vitest e React Testing Library.
- Playwright para testes de ponta a ponta.

Use as tecnologias que fizerem sentido para o produto. Não instale todas indiscriminadamente.

A interface deverá ser responsiva, rápida, acessível, consistente e preparada para celulares, tablets e computadores.

## Backend

Considere:

- Node.js em versão LTS apropriada.
- TypeScript.
- NestJS ou Fastify, escolhendo a alternativa que ofereça o melhor equilíbrio entre organização, desempenho e facilidade de manutenção.
- API REST versionada.
- Documentação OpenAPI.
- Zod, class-validator ou alternativa adequada para validação.
- Autenticação segura.
- Autorização baseada em papéis e permissões.
- Serviços de aplicação separados das rotas e controladores.
- Tratamento centralizado de erros.
- Logs estruturados.
- Limitação de requisições.
- Processamento assíncrono de tarefas quando necessário.

Não coloque toda a lógica de negócio em um único arquivo.

## Banco de dados

Avalie PostgreSQL como banco principal.

Considere:

- Prisma ou Drizzle ORM.
- PostGIS, se as funcionalidades geográficas justificarem seu uso.
- Migrações versionadas.
- Índices adequados.
- Transações para operações financeiras ou de créditos.
- Restrições de integridade.
- Estratégias de backup e restauração.

Utilize Redis somente quando houver uma necessidade real, como cache, filas ou limitação distribuída de requisições.

## Infraestrutura

Prepare a aplicação para:

- Frontend hospedado na Hostinger ou em serviço equivalente compatível.
- Backend hospedado no Render ou em alternativa adequada.
- Código-fonte versionado no GitHub.
- Banco de dados gerenciado.
- HTTPS.
- Ambientes separados de desenvolvimento, homologação e produção.
- Integração contínua.
- Implantação reproduzível.
- Monitoramento de erros e disponibilidade.
- Backups e recuperação de desastres.

Não presuma que todos os serviços externos estão configurados.

Produza instruções claras para conectar os serviços, configurar variáveis de ambiente e realizar a primeira publicação.

Caso seja mais adequado manter frontend e backend em serviços diferentes, explique como conectá-los corretamente.

---

# 5. EXPERIÊNCIA DO USUÁRIO

Crie uma identidade visual própria, profissional e contemporânea.

O produto deve transmitir:

- Confiança.
- Utilidade.
- Modernidade.
- Participação comunitária.
- Transparência.
- Segurança.
- Facilidade de utilização.

Evite uma interface genérica que pareça um template pronto sem personalidade.

Crie um sistema de design com:

- Paleta de cores.
- Tipografia.
- Espaçamentos.
- Componentes reutilizáveis.
- Botões.
- Campos de formulário.
- Cartões.
- Modais.
- Alertas.
- Estados de carregamento.
- Estados vazios.
- Mensagens de erro.
- Confirmações de ações.
- Componentes acessíveis.

A navegação deverá ser simples e organizada.

Considere as seguintes áreas principais:

1. Início.
2. Mapa.
3. Comunidade.
4. Recompensas.
5. Perfil.

A área de recompensas poderá permanecer desativada até que sua versão esteja implementada.

As páginas comerciais deverão ser incorporadas progressivamente.

Não sobrecarregue a tela inicial. Utilize pesquisas com usuários e testes de usabilidade para orientar as decisões.

---

# 6. CADASTRO E AUTENTICAÇÃO

Implemente:

- Cadastro de usuários.
- Login.
- Logout.
- Recuperação de senha.
- Verificação de e-mail, quando apropriada.
- Gerenciamento seguro de sessões.
- Proteção contra tentativas automatizadas de login.
- Perfil público.
- Configurações de privacidade.
- Preferências de notificações.
- Exclusão de conta conforme as regras aplicáveis.
- Solicitação de acesso e correção de dados pessoais.
- Encerramento de sessões quando necessário.

Utilize mecanismos de autenticação seguros e compatíveis com a arquitetura escolhida.

Não crie um sistema caseiro de criptografia.

Se utilizar cookies de sessão, configure corretamente atributos como HttpOnly, Secure e SameSite, conforme o contexto.

Implemente autorização no servidor.

Um usuário não poderá acessar dados privados de outro usuário simplesmente modificando o identificador enviado à API.

---

# 7. CATÁLOGO DE ESTABELECIMENTOS

A plataforma deverá possuir um catálogo de negócios e serviços locais.

Os usuários deverão conseguir:

- Pesquisar estabelecimentos por nome.
- Pesquisar por categoria.
- Filtrar por cidade ou região.
- Consultar páginas públicas.
- Visualizar avaliações.
- Consultar informações comerciais.
- Encontrar promoções disponíveis.
- Sugerir novos estabelecimentos.
- Solicitar correções.
- Informar que um negócio aparentemente está fechado.
- Denunciar informações incorretas.

As páginas comerciais poderão ser cadastradas inicialmente com informações públicas obtidas de fontes cujo uso seja permitido.

Um estabelecimento poderá existir no catálogo mesmo que seu proprietário ainda não tenha criado uma conta.

Nesse caso, a página deverá exibir claramente o status:

"Página ainda não reivindicada pelo responsável."

Não apresente um estabelecimento como verificado sem que o processo de verificação tenha sido concluído.

Implemente um mecanismo para o responsável legítimo reivindicar e administrar a página.

O processo deverá prever:

- Verificação de vínculo com o estabelecimento.
- Aprovação ou rejeição.
- Tratamento de páginas duplicadas.
- Contestação.
- Histórico das decisões.
- Auditoria das alterações importantes.

Não copie indiscriminadamente dados de outros serviços. Verifique as licenças e os termos de uso das fontes utilizadas.

---

# 8. MAPA E DESCOBERTA LOCAL

Implemente uma experiência geográfica que permita encontrar estabelecimentos próximos ou em regiões selecionadas.

Considere:

- Mapa interativo.
- Marcadores de estabelecimentos.
- Busca por localização.
- Filtros por categoria.
- Lista de resultados sincronizada com o mapa.
- Página detalhada do estabelecimento.
- Promoções ativas.
- Alternativa em formato de lista quando o mapa não estiver disponível.

Permita que o usuário informe uma cidade ou região manualmente.

A localização do dispositivo deverá ser opcional quando não for indispensável.

Não publique a localização precisa dos usuários.

Não implemente rastreamento contínuo como requisito para usar o produto.

Escolha um provedor de mapas após comparar qualidade, custos, licenças, limites e facilidade de integração.

---

# 9. SISTEMA DE AVALIAÇÕES

Permita que os consumidores avaliem estabelecimentos dentro da própria plataforma.

Considere:

- Nota.
- Comentário opcional.
- Data da avaliação.
- Histórico de atualização.
- Denúncia de conteúdo.
- Resposta pública de comerciantes verificados.
- Moderação.
- Indicadores agregados.
- Filtros e ordenação.
- Identificação transparente do nível de evidência disponível.

O sistema deverá distinguir opinião de comprovação.

Uma avaliação verificada não significa automaticamente que seu conteúdo seja verdadeiro.

Uma avaliação sem comprovação não deverá ser automaticamente considerada falsa.

Implemente critérios de evidência compreensíveis para o público.

## Níveis de evidência sugeridos

Nível 1 — Avaliação sem comprovação independente.

Nível 2 — Presença estimada, baseada em sinais permitidos e consentidos.

Nível 3 — Interação confirmada, por meio de QR code ou código válido.

Nível 4 — Compra confirmada, mediante evidência tecnicamente confiável.

Cada nível deverá explicar o que realmente foi confirmado.

A simples leitura de um QR code não prova necessariamente uma compra.

A localização GPS isolada também não comprova de forma absoluta uma visita.

Implemente controles para reduzir falsificações, duplicações e reutilizações abusivas.

Não revele informações sensíveis utilizadas internamente na prevenção a fraudes.

Não utilize métodos secretos para atribuir notas maiores a estabelecimentos pagantes.

Não permita que comerciantes comprem avaliações positivas ou removam críticas legítimas apenas por não gostarem delas.

---

# 10. COMUNIDADE LOCAL

Crie uma comunidade que estimule o uso frequente da plataforma.

O usuário deverá conseguir:

- Publicar textos.
- Consultar publicações públicas da região.
- Comentar.
- Reagir a publicações.
- Seguir outros usuários.
- Consultar perfis públicos.
- Denunciar conteúdo.
- Bloquear outros usuários.
- Controlar informações públicas do próprio perfil.

O feed deverá permitir organização por cidade, região ou categorias apropriadas.

Não exiba automaticamente a localização precisa do autor.

Implemente limites contra spam, assédio e automação abusiva.

Defina regras de moderação e um processo para analisar denúncias.

As mensagens privadas deverão ser implementadas em uma atualização posterior.

Nessa etapa, as mensagens privadas deverão obedecer à regra de relacionamento mútuo definida pelo produto.

Implemente solicitações de mensagem quando necessário, bloqueios, controles de privacidade e medidas contra assédio.

---

# 11. SISTEMA DE RECOMPENSAS

Desenvolva um sistema de créditos promocionais internos.

Esses créditos deverão incentivar participação legítima e aproximar consumidores de negócios locais.

Inicialmente, não implemente criptomoeda negociável nem transferência de créditos entre usuários.

Implemente:

- Conta de créditos.
- Saldo disponível.
- Histórico de movimentações.
- Créditos recebidos.
- Débitos.
- Estornos.
- Expiração, quando aplicável.
- Regras de participação.
- Identificação da campanha que originou cada recompensa.
- Controles contra duplicação de recompensas.
- Limites de participação.
- Auditoria.

Utilize um livro-razão de movimentações consistente e reconciliável.

O sistema deverá ser resistente a falhas de rede, solicitações repetidas e tentativas de manipulação.

Uma mesma ação não poderá gerar créditos duplicados indevidamente.

## Regra obrigatória

Nunca condicione a recompensa a uma avaliação positiva.

O usuário poderá expressar uma experiência positiva, negativa ou neutra sem alterar a elegibilidade da recompensa.

A plataforma poderá recompensar atividades como:

- Responder a pesquisas.
- Participar de campanhas.
- Fornecer feedback solicitado.
- Cumprir atividades promocionais claramente definidas.

Não recompense avaliações publicadas em serviços externos quando as regras desses serviços proibirem esse incentivo.

## Futuras possibilidades

Transferências entre usuários, conversão em dinheiro, saques, negociação, venda de créditos e tokenização somente poderão ser consideradas após análise jurídica, regulatória, contábil e de segurança.

Não prometa valorização dos créditos.

Não apresente créditos promocionais como investimento.

---

# 12. CAMPANHAS PROMOCIONAIS

Permita que comerciantes criem campanhas para atrair consumidores.

Exemplo:

"Os primeiros seis participantes que concluírem a pesquisa de satisfação hoje receberão dez créditos promocionais."

Cada campanha deverá possuir:

- Estabelecimento responsável.
- Nome.
- Descrição.
- Período de validade.
- Regras de participação.
- Quantidade máxima de participantes.
- Recompensa.
- Orçamento máximo.
- Limite por usuário.
- Estado da campanha.
- Registro das participações.
- Critérios de elegibilidade.
- Histórico de encerramento.

Implemente validação no servidor.

Não confie apenas nos valores enviados pelo navegador.

Não permita que uma campanha ultrapasse seu orçamento definido.

O sistema deverá impedir que o mesmo usuário explore falhas para receber recompensas indevidas.

O comerciante deverá visualizar resultados agregados e respeitar a privacidade dos participantes.

---

# 13. ÁREA DO COMERCIANTE

Desenvolva a área comercial em uma atualização posterior.

O comerciante verificado deverá conseguir:

- Administrar informações autorizadas da página.
- Atualizar horários e contatos.
- Responder a avaliações.
- Criar campanhas.
- Consultar campanhas anteriores.
- Visualizar indicadores permitidos.
- Gerenciar permissões de funcionários, se essa funcionalidade for incluída.
- Consultar o plano contratado.
- Acessar relatórios conforme suas permissões.

O painel gratuito deverá manter as funções essenciais de administração da página.

Os planos pagos poderão oferecer análises avançadas.

O pagamento de uma assinatura nunca poderá permitir manipular a nota pública do estabelecimento.

Não permita que comerciantes visualizem dados pessoais desnecessários, localização precisa de consumidores ou mensagens privadas.

---

# 14. INTELIGÊNCIA COMERCIAL E INTELIGÊNCIA ARTIFICIAL

Em uma atualização avançada, crie um sistema de inteligência para ajudar comerciantes a compreender a experiência dos consumidores.

A IA poderá analisar feedbacks autorizados e produzir:

- Resumos de opiniões.
- Principais elogios.
- Problemas recorrentes.
- Sugestões de melhoria.
- Evolução de temas ao longo do tempo.
- Mudanças relevantes na percepção dos consumidores.
- Relatórios periódicos.
- Recomendações práticas.
- Comparações temporais adequadas.

Utilize modelos de IA por meio de integrações oficiais e configuráveis.

Não deixe chaves de API expostas no navegador.

Não envie dados pessoais desnecessários aos provedores de IA.

Implemente limites de custo e monitore o consumo.

A IA deverá distinguir observações presentes nos dados de hipóteses e recomendações.

Não invente estatísticas.

Não apresente conclusões fortes com amostras pequenas.

Quando os dados forem insuficientes, informe essa limitação.

Sempre que possível, permita rastrear cada conclusão até os dados agregados que a sustentam.

Não exponha ao comerciante a identidade de consumidores quando isso não for necessário e autorizado.

---

# 15. ASSINATURAS E MONETIZAÇÃO

Implemente a monetização somente depois de estabelecer uma base funcional de consumidores e comerciantes.

Considere:

- Plano gratuito.
- Planos pagos.
- Gestão de assinaturas.
- Controle de acesso por plano.
- Histórico de cobrança.
- Cancelamento.
- Tratamento de falhas de pagamento.
- Integração com provedor de pagamento adequado.
- Webhooks autenticados.
- Controle contra processamento duplicado de eventos.
- Faturamento e documentação conforme as obrigações aplicáveis.

Não armazene dados completos de cartões de pagamento se isso puder ser evitado.

A monetização deverá ocorrer por ferramentas legítimas, campanhas e inteligência comercial, não pela venda de avaliações positivas.

---

# 16. SEGURANÇA E PRIVACIDADE

A segurança deverá fazer parte da arquitetura desde a primeira versão.

Implemente:

- Validação de entradas.
- Controle de permissões.
- Proteção contra injeções.
- Proteção contra XSS.
- Proteções CSRF quando aplicáveis.
- Rate limiting.
- Gestão segura de sessões.
- Política adequada de CORS.
- Proteção contra abuso de autenticação.
- Logs de auditoria.
- Gestão de segredos.
- Backups.
- Monitoramento de erros.
- Atualizações de dependências.
- Procedimentos de recuperação.
- Separação entre desenvolvimento e produção.

Considere a LGPD brasileira e as obrigações aplicáveis ao tratamento de dados pessoais.

Documente os dados coletados, a finalidade, o acesso e os períodos de retenção.

Solicite permissões de localização apenas quando necessário.

Não guarde históricos detalhados de localização sem justificativa válida.

Não exponha e-mails, telefones privados, documentos, tokens ou dados de autenticação.

Se o produto puder ser utilizado por menores de idade, avalie especificamente as exigências de proteção, privacidade, publicidade e comunicação antes de liberar os recursos correspondentes.

Crie termos de uso, política de privacidade, regras da comunidade e política de recompensas como documentos que deverão passar por revisão jurídica antes da publicação.

---

# 17. MODERAÇÃO E PREVENÇÃO A FRAUDES

Crie mecanismos para:

- Identificar spam.
- Detectar duplicações suspeitas.
- Limitar ações abusivas.
- Investigar denúncias.
- Moderar conteúdo.
- Suspender contas conforme regras transparentes.
- Permitir contestação.
- Registrar decisões administrativas.
- Prevenir recompensas duplicadas.
- Detectar abuso de campanhas.
- Tratar páginas comerciais falsas.
- Impedir acessos não autorizados.

Não utilize apenas um indicador para punir usuários automaticamente.

Crie mecanismos de revisão humana para decisões sensíveis.

A prevenção a fraudes deverá respeitar a privacidade e evitar falsos positivos desnecessários.

---

# 18. ADMINISTRAÇÃO DA PLATAFORMA

Crie uma área administrativa separada e protegida.

O administrador autorizado deverá conseguir:

- Consultar usuários conforme suas permissões.
- Analisar denúncias.
- Moderar publicações e avaliações.
- Gerenciar estabelecimentos.
- Analisar reivindicações comerciais.
- Suspender campanhas fraudulentas.
- Investigar movimentações suspeitas de créditos.
- Consultar registros de auditoria.
- Gerenciar categorias e configurações permitidas.
- Acompanhar indicadores operacionais.

Implemente autenticação forte e princípio do menor privilégio.

Toda ação administrativa relevante deverá ser registrada.

Não permita que qualquer usuário se torne administrador modificando dados enviados pelo frontend.

---

# 19. TESTES E QUALIDADE

Implemente testes automatizados em todas as etapas.

Considere:

- Testes unitários.
- Testes de integração.
- Testes de API.
- Testes de autenticação.
- Testes de autorização.
- Testes de componentes.
- Testes de ponta a ponta.
- Testes responsivos.
- Testes de segurança.
- Testes de carga proporcionais à escala esperada.
- Testes de restauração de backups.

Priorize especialmente os testes de:

1. Cadastro e autenticação.
2. Proteção de dados privados.
3. Avaliações.
4. Permissões comerciais.
5. Créditos e campanhas.
6. Prevenção de duplicações.
7. Denúncias e moderação.
8. Assinaturas e pagamentos.
9. Processamento de webhooks.
10. Integridade dos dados.

Não declare os testes aprovados sem executá-los.

Se um teste falhar, identifique a causa, corrija o problema e execute novamente.

---

# 20. DESENVOLVIMENTO POR VERSÕES

Não tente construir tudo de uma vez.

Organize o trabalho nas seguintes versões.

## VERSÃO 1 — MVP PARA PUBLICAÇÃO

Implementar:

- Fundação técnica.
- Frontend.
- Backend.
- Banco de dados.
- Cadastro e autenticação.
- Catálogo de estabelecimentos.
- Pesquisa.
- Mapa.
- Páginas públicas.
- Avaliações.
- Feed comunitário básico.
- Perfis públicos.
- Seguimento de usuários.
- Denúncias.
- Moderação administrativa.
- Segurança.
- Testes.
- Documentação.
- Implantação.

O objetivo é colocar no ar uma primeira versão realmente utilizável.

Não incluir nessa versão recursos complexos de criptoativos, transferências de créditos ou inteligência comercial avançada.

## ATUALIZAÇÃO 1 — VERIFICAÇÃO E CONFIANÇA

Implementar:

- Níveis de evidência.
- QR codes.
- Códigos de participação.
- Controles antifraude.
- Histórico de evidências.
- Contestação.
- Melhorias na transparência das avaliações.

## ATUALIZAÇÃO 2 — RECOMPENSAS

Implementar:

- Créditos promocionais.
- Carteira interna.
- Histórico de movimentações.
- Campanhas.
- Limites.
- Expiração quando aplicável.
- Estornos.
- Auditoria.
- Proteção contra duplicações.

## ATUALIZAÇÃO 3 — COMUNIDADE AVANÇADA

Implementar:

- Mensagens privadas conforme a regra de relacionamento mútuo.
- Bloqueios.
- Solicitações de mensagem.
- Controles de privacidade.
- Melhorias no feed.
- Notificações.
- Moderação avançada.

## ATUALIZAÇÃO 4 — COMERCIANTES

Implementar:

- Reivindicação de páginas.
- Verificação de responsáveis.
- Painel comercial.
- Gestão de informações.
- Campanhas.
- Respostas às avaliações.
- Relatórios básicos.

## ATUALIZAÇÃO 5 — INTELIGÊNCIA E MONETIZAÇÃO

Implementar:

- Planos pagos.
- Assinaturas.
- Dashboard avançado.
- Análises agregadas.
- Resumos com IA.
- Identificação de problemas recorrentes.
- Recomendações comerciais.
- Relatórios exportáveis.
- Monitoramento de custos e desempenho.

Ao concluir a Atualização 5, considere implementada a visão do produto definida neste documento, desde que todos os critérios de aceite tenham sido atendidos.

Isso não significa que o projeto acabou definitivamente. Novas ideias serão organizadas como Atualização 6, Atualização 7 e assim por diante.

---

# 21. COMO VOCÊ DEVERÁ TRABALHAR NO REPOSITÓRIO

Se você possuir acesso aos arquivos do projeto, siga este procedimento.

Primeiro, inspecione o repositório completo.

Identifique:

- Estrutura atual.
- Tecnologias já instaladas.
- Funcionalidades existentes.
- Estado do frontend.
- Estado do backend.
- Banco de dados.
- Configurações de ambiente.
- Scripts.
- Testes.
- Problemas conhecidos.
- Integrações existentes.

Não sobrescreva indiscriminadamente arquivos existentes.

Não remova funcionalidades que já estejam funcionando sem necessidade e sem explicar o motivo.

Preserve configurações válidas e identifique possíveis incompatibilidades.

Depois, apresente um diagnóstico técnico objetivo e um plano de execução.

Em seguida, implemente o trabalho em etapas pequenas e verificáveis.

Se houver autorização para executar comandos, utilize-os para instalar dependências, executar testes, verificar compilações e identificar erros.

Não instale dependências de forma indiscriminada.

Não altere configurações de produção sem avaliar os impactos.

Não publique alterações destrutivas no banco de dados sem backup e autorização.

Se precisar de uma decisão minha, formule uma pergunta específica e explique por que ela é necessária.

Não invente credenciais ou segredos.

Não envie informações sensíveis para ferramentas externas sem autorização apropriada.

---

# 22. DOCUMENTAÇÃO OBRIGATÓRIA

Mantenha atualizados:

- README.md.
- Documento de arquitetura.
- Modelo de dados.
- Documentação da API.
- Instruções de instalação.
- Variáveis de ambiente necessárias.
- Instruções de desenvolvimento local.
- Instruções de implantação.
- Instruções de backup e restauração.
- Estratégia de testes.
- Histórico das versões.
- Decisões técnicas importantes.
- Limitações conhecidas.
- Próximas tarefas.

Crie um arquivo de progresso do projeto, por exemplo:

docs/STATUS_DO_PROJETO.md

Esse arquivo deverá indicar:

- Versão atual.
- Funcionalidades concluídas.
- Funcionalidades parcialmente concluídas.
- Funcionalidades pendentes.
- Testes executados.
- Testes que falharam.
- Problemas conhecidos.
- Dependências externas.
- Próximas ações.

Atualize esse arquivo ao terminar cada etapa.

---

# 23. CRITÉRIOS PARA CONSIDERAR UMA VERSÃO CONCLUÍDA

Uma versão só poderá ser considerada concluída quando:

1. As funcionalidades previstas estiverem implementadas.
2. O frontend estiver conectado ao backend real.
3. Os dados estiverem sendo persistidos corretamente.
4. As regras de autorização estiverem implementadas no servidor.
5. Os testes aplicáveis tiverem sido executados.
6. Os problemas críticos conhecidos estiverem resolvidos.
7. A documentação estiver atualizada.
8. A implantação em homologação estiver validada.
9. As variáveis de ambiente estiverem documentadas.
10. Os critérios de aceite estiverem satisfeitos.

Se algum item não puder ser concluído, registre explicitamente a limitação.

Não apresente um protótipo como produto pronto.

Não apresente uma tela como integração funcional se os botões não executarem ações reais.

Não declare a plataforma pronta para produção sem verificar os requisitos de segurança, operação e privacidade.

---

# 24. SUA PRIMEIRA TAREFA

Comece agora.

Não tente implementar a plataforma inteira em uma única resposta.

Primeiro:

1. Inspecione o repositório e o ambiente disponível.
2. Identifique as tecnologias e funcionalidades já existentes.
3. Produza um diagnóstico do estado atual.
4. Defina a arquitetura recomendada.
5. Elabore o plano de execução da Versão 1.
6. Identifique dependências externas e decisões realmente necessárias.
7. Implemente a primeira etapa autorizada.
8. Execute os testes possíveis.
9. Documente os resultados.
10. Apresente o que foi efetivamente realizado e o que ainda falta.

Se não existir um repositório, prepare a estrutura inicial do projeto e as instruções necessárias para executá-lo localmente.

Se não houver acesso direto ao ambiente, forneça arquivos completos, instruções de instalação e comandos executáveis, sem afirmar que realizou operações que não pôde executar.

A prioridade absoluta é construir uma base técnica sólida e entregar uma primeira versão funcional, segura e publicável.

A partir dela, evolua progressivamente até concluir as funcionalidades previstas na Atualização 5.

Pense como uma equipe responsável por construir um produto real, que precisará conquistar usuários, funcionar de maneira confiável, proteger dados pessoais, evitar fraudes e sustentar um negócio.