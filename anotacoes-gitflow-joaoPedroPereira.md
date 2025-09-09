# Segurança em Banco de Dados

**Objetivo:** proteger os dados contra acessos não autorizados, perda ou corrupção.

## Principais mecanismos:

- **Controle de acesso e autenticação:** uso de senhas fortes, MFA/biometria, RBAC (permissões por papéis), revisão de privilégios.

- **Criptografia:** em trânsito (TLS/SSL) e em repouso (TDE, Always Encrypted).

- **Prevenção de injeção SQL:** queries parametrizadas, stored procedures, WAFs.

- **Auditoria e monitoramento:** logging de acessos, Database Activity Monitoring (DAM).

- **Backup e recuperação:** regra 3-2-1, backups criptografados e testados.

- **Hardenização:** isolamento de ambientes, firewall, atualização contínua, gestão segura de credenciais.

---

# Integridade em Banco de Dados

**Objetivo:** manter os dados corretos, consistentes e válidos.

## Tipos de integridade:

- **De domínio:** restringe valores permitidos (ex.: idade > 0).

- **De entidade:** garante unicidade com chaves primárias.

- **Referencial:** assegura consistência entre tabelas com foreign keys.

- **De usuário/negócio:** regras específicas do sistema (ex.: limite de crédito).

- **Controle de isolamento (ACID):** evita problemas em transações concorrentes.

---

# Blockchain e Integridade

**Conceito:** livro-razão distribuído, imutável e seguro.

**Funcionamento:** transações agrupadas em blocos, validadas por consenso e encadeadas via hash.

## Relação com integridade:

- **Entidade** → transações únicas e assinadas.

- **Referencial** → blocos encadeados (confiança).

- **Domínio** → só aceita transações válidas pelo protocolo.