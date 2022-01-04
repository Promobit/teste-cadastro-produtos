# Desafio Promobit

⚠️ **Atenção**: Esse teste possui uma etapa de lógica e uma etapa prática, para fazer o teste de lógica acesse: [teste-logica](https://github.com/Promobit/teste-logica)

- [Desafio Promobit](#desafio-promobit)
  - [Objetivo](#objetivo)
  - [Desafio](#desafio)
  - [Requisitos](#requisitos)
  - [Techs](#techs-obrigatrio)
  - [Como entregar](#como-entregar)
  
## Objetivo
O objetivo é avaliar o seu conhecimento e habilidades em desenvolvimento Back-End e Front-End.

### Desafio
Criação de CRUD de produtos, tags e extração de relatório de relevância de produtos.

### Requisitos
- Páginas de listagem/cadastro/edição/delete de `Produtos`, as páginas devem ter navegação entre elas.
- Páginas de listagem/cadastro/edição/delete de `Tags`, as páginas devem ter navegação entre elas. 
- Relatório de relevância de produtos.
- Poderá ser vinculadas uma ou mais `Tags` pela tela de cadastro ou edição de `Produtos`.

#### Regras para extração de relatório de releavância de produtos 
- SQL com listagem de `Tags` mais um sumarizador de `Produtos` atrelado a cada `Tag`;

#### Estrutura das tabelas envolvidas:
```SQL
CREATE TABLE `product` (
  `id` int NOT NULL AUTO_INCREMENT,
  `name` varchar(50) NOT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `name_UNIQUE` (`name`)
);
CREATE TABLE `tag` (
  `id` int NOT NULL AUTO_INCREMENT,
  `name` varchar(50) NOT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `name_UNIQUE` (`name`)
);
CREATE TABLE `product_tag` (
   `product_id` int NOT NULL,
   `tag_id` int NOT NULL,
   PRIMARY KEY (`product_id`,`tag_id`),
   CONSTRAINT `product_id` FOREIGN KEY (`product_id`) REFERENCES `product` (`id`),
   CONSTRAINT `tag_id` FOREIGN KEY (`tag_id`) REFERENCES `tag` (`id`)
);
```

### Techs (Obrigatório)

- PHP 7+ 
- MySQL 5.7+
- Pode usar qualquer framework PHP para o desenvolvimento ou não usar nenhum, fica a sua escolha.
- Pode usar qualquer framework de Front, tais como: Bootstrap, Material UI, etc...

### Seria bom se fizesse (Opcional)

- Autenticação de usuário.
- Docker + Docker compose.

### Como entregar

- Colocar SQL de extração de relatório de relevancia de produtos no README.md do seu repositório.
- Envie o link do seu repositório para [contato@promobit.com.br](mailto:contato@promobit.com.br)

### Orientações
- Procure fazer um código sucinto. 
- Coloque isso em um repositório GIT.
- Colocar as orientações de setup no README do seu repositório.
- Fique avontade para incrementar o projeto, nos surpreenda.

# Boa sorte 
