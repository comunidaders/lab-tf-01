### Descrição da Tarefa: Criação de Módulos Terraform para EC2, S3 e Security Group

**Objetivo:**

Desenvolver três módulos Terraform reutilizáveis utilizando módulos da comunidade para:

1. **Criar uma instância EC2:**
   - Utilizando uma subnet criada pelo módulo de VPC.
   - Associar um security group criado pelo módulo de security group.

2. **Criar um bucket S3:**
   - Nome especificado pelo usuário.
   - Configurações básicas como versionamento.

3. **Criar um Security Group:**
   - Definir regras com CIDR criado pelo módulo de security group.

**Instruções:**

1. **Módulo EC2:**
   - Variáveis principais: `instance_type`, `ami_id`, `subnet_id`, `security_group_ids`.
   - Saídas principais: `instance_id`, `public_ip`.

2. **Módulo S3:**
   - Variáveis principais: `bucket_name`, `versioning`.
   - Saídas principais: `bucket_arn`, `bucket_domain_name`.

3. **Módulo Security Group:**
   - Variáveis principais: `vpc_id`, `cidr_blocks`.
   - Saída principal: `security_group_id`.

**Passos:**

1. Clone o repositório com os módulos.
2. Configure os módulos com as variáveis necessárias.
3. Execute `terraform init`, `terraform plan` e `terraform apply` para criar os recursos.
