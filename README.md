# Sistema de Gestão de Clientes COBOL

## Descrição
Sistema de gestão de clientes desenvolvido em COBOL para cadastro, consulta, alteração e exclusão de dados de clientes, além de geração de relatórios.

## Informações do Projeto
- **Autor:** CAIO
- **Empresa:** X
- **Data:** 27/06/2025
- **Linguagem:** COBOL
- **Objetivo:** Sistema de Gestão de Clientes (originalmente documentado como "SISTEMA DE GESTAO DE FLIMES")

## Estrutura de Arquivos

### Arquivos do Sistema
- `CLIENTES.cob` - Programa principal em COBOL
- `CLIENTES.DAT` - Arquivo de dados indexado dos clientes
- `RELATO.TXT` - Arquivo de relatório gerado pelo sistema

### Estrutura de Dados
O sistema armazena as seguintes informações para cada cliente:
- **Telefone** (9 dígitos) - Chave primária
- **Nome** (até 30 caracteres)
- **Email** (até 40 caracteres)

## Funcionalidades

O sistema oferece um menu interativo com as seguintes opções:

### 1. Incluir Cliente
- Permite cadastrar novos clientes no sistema
- Valida se o telefone (chave) já existe
- Exibe mensagem de erro caso o cliente já esteja cadastrado

### 2. Consultar Cliente
- Busca cliente pelo número de telefone
- Exibe dados completos quando encontrado
- Informa quando o cliente não é encontrado

### 3. Alterar Cliente
- Permite modificar dados de clientes existentes
- Busca pelo telefone e permite editar nome e email
- Confirma se a alteração foi realizada com sucesso

### 4. Excluir Cliente
- Remove clientes do sistema
- Solicita confirmação antes da exclusão (S/N)
- Valida se o registro existe antes de excluir

### 5. Relatório em Tela
- Exibe todos os clientes cadastrados na tela
- Paginação automática (5 registros por tela)
- Mostra contador total de registros

### 6. Relatório em Disco
- Gera arquivo de relatório (RELATO.TXT) com todos os clientes
- Exporta dados para arquivo sequencial
- Mostra contador de registros processados

### X. Sair
- Encerra o sistema

## Requisitos Técnicos

### Ambiente
- Compilador COBOL compatível
- Sistema operacional Windows (conforme caminho dos arquivos)
- Suporte a arquivos indexados

### Caminhos dos Arquivos
```
C:\Users\Windows\Cobol\ProjetoFinalCobol\CLIENTES.DAT
C:\Users\Windows\Cobol\ProjetoFinalCobol\RELATO.TXT
```

## Como Executar

1. **Compilação:**
   ```bash
   # Compile o arquivo CLIENTES.cob usando seu compilador COBOL
   cobc -x CLIENTES.cob -o CLIENTES.exe
   ```

2. **Execução:**
   ```bash
   # Execute o programa
   CLIENTES.exe
   ```

3. **Primeira Execução:**
   - O sistema criará automaticamente o arquivo CLIENTES.DAT caso não exista
   - O arquivo será criado como arquivo indexado com organização dinâmica

## Características Técnicas

### Organização dos Arquivos
- **CLIENTES.DAT:** Arquivo indexado com acesso dinâmico
- **RELATO.TXT:** Arquivo sequencial para relatórios

### Interface do Usuário
- Interface baseada em terminal com cores
- Telas organizadas com campos de entrada específicos
- Mensagens de erro contextualizadas
- Sistema de navegação por menu numérico

### Tratamento de Erros
- Validação de chaves duplicadas
- Verificação de registros não encontrados
- Status de arquivo para controle de operações
- Mensagens informativas para o usuário

## Estrutura do Menu

```
SISTEMA DE CLIENTES
═══════════════════

1 - INCLUIR
2 - CONSULTAR  
3 - ALTERAR
4 - EXCLUIR
5 - RELATORIO EM TELA
6 - RELATORIO EM DISCO
X - SAIDA

OPCAO........: _
```

## Exemplo de Dados
O arquivo RELATO.TXT contém exemplos de registros:
- Cliente: CAIO DE SOUZA GOMES SANTIAGO (Tel: 992321111)
- Cliente: VITORIA (Tel: 992324339)


---
*Sistema desenvolvido em COBOL para fins educacionais e de gestão básica de clientes.*
