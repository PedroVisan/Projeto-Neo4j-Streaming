# Projeto Neo4j - Streaming Graph

Este projeto contém o banco de dados que criei no Neo4j, incluindo usuários, filmes, séries,
atores e diretores, com relacionamentos como WATCHED (com propriedade rating), ACTED_IN, DIRECTED_BY e HAS_GENRE.

## Como usar

1. Abra o **Neo4j Desktop** ou **Neo4j Aura**.
2. Crie um **novo banco de dados**.
3. Copie os arquivos CSV da pasta `data/` para o diretório de importação do Neo4j.
4. Importe os nós:
```cypher
LOAD CSV WITH HEADERS FROM 'file:///node-export.csv' AS row
CREATE (n:Label {nome: row.nome});

OU

Abra image/bloom-visualization-streaming.png para visualizar
