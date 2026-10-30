# Recursos que exigem credenciais ou integrações externas

Regra: todos os itens abaixo devem ser **novos e exclusivos desta plataforma**. Nenhum
credencial, banco ou serviço do site atual pode ser reutilizado.
Os provedores citados são exemplos, não escolhas feitas. Nada abaixo está configurado.

| Recurso | Para que | Na V1? | Status |
|---|---|---|---|
| Repositório GitHub novo | Código e CI | Sim | Não criado (sem acesso a GitHub nesta sessão) |
| Banco de dados PostgreSQL gerenciado, novo | Dados da plataforma | Sim | Não configurado |
| Autenticação (e-mail/senha ou provedor) | Contas e login | Sim | Não configurado |
| Login social (ex.: Google OAuth) | Entrada facilitada | Opcional | Não configurado |
| Mapas e geocodificação (ex.: Google Maps, Mapbox, OpenStreetMap) | Busca por local, mapa | Sim | Provedor não escolhido |
| E-mail transacional | Confirmação de conta, recuperação de senha | Sim | Não configurado |
| Armazenamento de imagens | Fotos de locais e avaliações | A decidir | Não configurado |
| Hospedagem nova | Publicação futura | Só preparar | Não conectada, sem autorização |
| Domínio / DNS | Endereço público | Não | Não será tocado sem autorização explícita |
| Monitoramento de erros | Diagnóstico | Opcional | Não configurado |
| Pagamentos / resgate com parceiros | Recompensas reais | Não (futuro) | Fora da V1 |

## Como tratar credenciais

- Valores reais somente em `.env` local ou no cofre de segredos do provedor novo.
- `.env.example` lista apenas os nomes das variáveis.
- Chaves de desenvolvimento e de produção separadas, com permissões mínimas e restrição por
  domínio quando o provedor permitir.
- O dono cria ou autoriza cada conta. Claude não cria contas nem guarda segredos no repositório.
