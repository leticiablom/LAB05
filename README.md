# LAB05 - GraphQL vs REST - Um experimento controlado

## Passo 1: Desenho do Experimento

### A. Hipóteses

- **Hipótese Nula (H0)**:  
  As respostas às consultas GraphQL **não são mais rápidas** que as respostas REST, e o **tamanho das respostas GraphQL não é menor** que o das respostas REST.

- **Hipótese Alternativa (H1)**:  
  As respostas às consultas GraphQL **são mais rápidas** que as respostas REST (RQ1), e/ou as respostas GraphQL **têm tamanho menor** que as respostas REST (RQ2).

### B. Variáveis

- **Variáveis Dependentes**:
  - Tempo de resposta das consultas (para RQ1)
  - Tamanho das respostas (para RQ2)

- **Variável Independente**:
  - Tipo de API utilizada: GraphQL ou REST

### C. Tratamentos

- Execução de consultas usando uma API GraphQL
- Execução de consultas usando uma API REST

### D. Objetos Experimentais

- Conjunto de consultas representativas a serem executadas em ambas as APIs (GraphQL e REST)
- Bancos de dados ou serviços consultados por essas APIs

### E. Tipo de Projeto Experimental

- **Experimento controlado**, comparando o desempenho (tempo e tamanho de resposta) entre GraphQL e REST para as mesmas operações de consulta.

### F. Quantidade de Medições

- Para cada consulta e tipo de API, coletar um número suficiente de medições (por exemplo, **30 ou mais por consulta**) para garantir significância estatística.

### G. Ameaças à Validade

#### Validade Interna:
- Variações no ambiente de execução (carga do servidor, rede)
- Diferenças de implementação entre GraphQL e REST
- Tamanho e complexidade dos dados consultados

#### Validade Externa:
- Limitações na generalização para outros tipos de APIs ou domínios
- Consultas escolhidas podem não representar todas as possibilidades

#### Validade de Construção:
- Forma de medir tempo e tamanho da resposta
- Precisão das ferramentas de medição

#### Validade Estatística:
- Número insuficiente de medições
- Escolha inadequada de testes estatísticos

---

## Passo 2: Preparação do Experimento

### Desenvolvimento de Scripts

- Scripts para:
  - Enviar consultas para a API GraphQL
  - Enviar requisições para a API REST
  - Medir tempo de resposta
  - Medir tamanho da resposta
  - Registrar e armazenar dados de medição (tempo, tamanho, tipo de API)

### Consultas

- Definir um conjunto de consultas de exemplo com diferentes níveis de complexidade (simples, complexas, com múltiplas entidades)
- Garantir que as consultas em GraphQL e REST retornem os **mesmos dados** para permitir **comparação justa**

### Escolha de Bibliotecas/Ferramentas

- **Para o backend (APIs)**:
  - Node.js com Express/Apollo Server (GraphQL)
  - Node.js com Express (REST)
  - Alternativas: Flask, Django REST Framework (Python); Spring Boot (Java)

- **Para o banco de dados**:
  - PostgreSQL, MongoDB, MySQL (com dados de teste populados)

- **Para medição e automação**:
  - Python com:
    - `requests` (requisições HTTP)
    - `time` (medição de tempo)

- **Para análise de dados**:
  - `pandas`

- **Para visualização gráfica**:
  - `matplotlib`

### Configuração do Ambiente Experimental

- Configurar o servidor e o banco de dados
- Manter o ambiente **estável e controlado** para minimizar ruídos externos
- Documentar:
  - Versões de ferramentas
  - Configurações utilizadas
