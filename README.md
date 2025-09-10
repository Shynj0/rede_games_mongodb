# Atividade de Banco de Dados Não Relacional -- MongoDB

## Descrição

Exercício prático usando MongoDB com o banco `rede_games`, contendo as
coleções: - clientes - produtos - vendas

O objetivo é praticar comandos de inserção, consulta, atualização,
exclusão e agregação.

## Script Inicial

``` js
use rede_games

db.clientes.insertMany([
 { _id: 1, nome: "Marcos", idade: 25, cidade: "Fortaleza" },
 { _id: 2, nome: "Julia", idade: 30, cidade: "São Paulo" },
 { _id: 3, nome: "Lucas", idade: 19, cidade: "Recife" },
 { _id: 4, nome: "Ana", idade: 27, cidade: "Fortaleza" }
])

db.produtos.insertMany([
 { _id: 101, nome: "Mouse Gamer", categoria: "Periféricos", preco: 250 },
 { _id: 102, nome: "Teclado Mecânico", categoria: "Periféricos", preco: 400 },
 { _id: 103, nome: "CS:GO Deluxe", categoria: "Jogos", preco: 120 },
 { _id: 104, nome: "Headset Pro", categoria: "Periféricos", preco: 350 },
 { _id: 105, nome: "FIFA 25", categoria: "Jogos", preco: 300 }
])

db.vendas.insertMany([
 { clienteId: 1, produtoId: 101, quantidade: 1, data: "2024-05-01" },
 { clienteId: 1, produtoId: 103, quantidade: 2, data: "2024-05-03" },
 { clienteId: 2, produtoId: 102, quantidade: 1, data: "2024-05-02" },
 { clienteId: 3, produtoId: 105, quantidade: 1, data: "2024-05-04" },
 { clienteId: 4, produtoId: 104, quantidade: 2, data: "2024-05-05" }
])
```

## Questões

1.  Criar banco e coleções.
2.  Consultar clientes de Fortaleza.
3.  Consultar clientes de Fortaleza com idade \> 25.
4.  Mostrar nome e preço dos periféricos.
5.  Listar produtos entre 200 e 400 reais.
6.  Consultar clientes que não moram em Fortaleza e com idade \>= 20.
7.  Verificar campo `clienteVip` e listar clientes com idade tipo
    number.
8.  Inserir cliente Jorge (22, Salvador).
9.  Atualizar cidade de Marcos para Natal.
10. Atualizar Lucas com `status: ativo` e +1 idade.
11. Substituir documento de Julia.
12. Renomear `preco` → `valor` e remover `categoria`.
13. Remover produto FIFA 25.
14. Listar clientes de São Paulo ou Recife.
15. Usar `$lookup` para juntar vendas e produtos.
16. Agrupar total de produtos vendidos por categoria.
17. `$lookup` + `$group` para total por categoria.
18. Mostrar 2 produtos mais caros.
19. Mostrar do 3º ao 5º produto mais caro.

------------------------------------------------------------------------

📌 Autor: João Pedro Souza dos Anjos
