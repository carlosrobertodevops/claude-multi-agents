
# CLAUDE.md - Projeto OAuth Demo

## Mapa de Território

Este projeto implementa autenticação Auth. Use este arquivo como guardrail
antes de qualquer modificação - especialmente em contexto multi-agente.

## Módulos e Responsabilidades

### Backend ('src/api/' e 'src/middleware/")

- "src/api/auth.ts' - endpoints de autenticação (POST /auth/login ja existe)
- 'src/middleware/oauth.ts" - middleware OAuth (a criar)
- **Proprietário natural**: Subagente Backend

### Frontend (src/components/auth/\*)

- "src/components/auth/" - componentes React de autenticação
- "src/components/auth/LoginForm.tsx' já existe (não modificar)
- **Proprietário natural**: Subagente Frontend
  ##\* Testes (tests/")
- "tests/components/auth/" - testes unitários dos componentes
- **Proprietário natural**: Subagente Testes

## Contrato entre Módulos

O contrato da API OAuth está definido em docs/api/auth.md'.
Todos os subagentes devem seguir esse contrato sem alterá-lo.

## Arquivos Compartilhados - NÃO MODIFICAR sem aprovação humana

- "src/types/User.ts' - tipo User compartilhado por todos os módulos
- "src/config/env.ts' - variáveis de ambiente
- 'package. json' - dependências (não adicionar sem revisar)
- "tsconfig.json" - configuração TypeScript

## Regras para Subagentes

1. Cada subagente opera APENAS nos arquivos do seu escopo definido no prompt
2. Se precisar de um tipo de outro módulo, importe de "src/types/" - não crie duplicatas
3. Não criar arquivos fora do escopo definido
4. Dúvidas sobre o contrato → consultar "docs/api/auth.md", não improvisar
5. Ao terminar, listar todos os arquivos criados/modificados no relatório
