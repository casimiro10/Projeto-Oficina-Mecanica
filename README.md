Projeto Lógico de Banco de Dados - Oficina Mecânica

Este repositório contém o esquema lógico de banco de dados para o gerenciamento de ordens de serviço em uma oficina mecânica, desenvolvido como desafio de projeto da plataforma Digital Innovation One (DIO).

## 📌 Descrição do Desafio

O objetivo foi criar um esquema conceitual e lógico a partir do zero, baseando-se em uma narrativa de regras de negócio de uma oficina. O modelo estrutura o fluxo desde a entrada do veículo pelo cliente até a precificação final da Ordem de Serviço (OS), englobando peças e mão de obra.

## 🧠 Premissas Adotadas (Além da Narrativa)

Como solicitado no desafio, algumas informações não estavam explícitas na narrativa e foram preenchidas com base na lógica de sistemas reais:

- **Entidade `Cliente`:** A narrativa não especificava os atributos. Foram criados dados básicos essenciais como `Nome`, `CPF` (Unique) e `Telefone`.
- **Entidade `Veículo`:** Foram adicionados atributos padrão (`Placa` Unique, `Marca`, `Modelo`) e estabelecido o relacionamento 1:N com `Cliente`, assumindo que um cliente pode cadastrar múltiplos veículos na oficina.
- **Tabelas Associativas (N:M):** A narrativa cita que uma OS compõe múltiplos serviços e múltiplas peças. Para resolver isso no modelo relacional, foram criadas as tabelas de intersecção `OS_has_Peca` e `OS_has_Servico`, permitindo o cálculo dinâmico do valor total.

## 🗂️ Estrutura do Banco de Dados

O diagrama abaixo ilustra as entidades, atributos (PKs e FKs) e a cardinalidade dos relacionamentos:

![Esquema do Banco de Dados - Oficina](esquema_oficina.png)
*(Nota: Lembre-se de certificar que o nome do arquivo da imagem no repositório seja exatamente igual ao referenciado aqui).*
