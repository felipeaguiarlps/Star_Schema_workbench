# Star Schema para Cenário de Vendas

Este repositório contém a modelagem dimensional em forma de Star Schema

## Visão Geral do Projeto

A modelagem foi realizada no MySQL Workbench, com a criação de uma tabela fato e tabelas de dimensão para possibilitar uma análise eficiente dos dados relacionados aos professores. As dimensões são detalhadas por cursos, departamentos e datas de oferta, permitindo uma visualização clara do desempenho dos professores em diferentes contextos.

## Estrutura do Star Schema

### Tabela Fato

A tabela fato `Fato_Professores` contém os seguintes campos:
- **id_fato**: Identificador único da tabela fato.
- **id_professor**: Referência à tabela de dimensão de professores.
- **id_curso**: Referência à tabela de dimensão de cursos.
- **id_departamento**: Referência à tabela de dimensão de departamentos.
- **id_data_oferta**: Referência à tabela de dimensão de datas.
- **carga_horaria**: Total de horas ministradas pelo professor no curso.
- **salario**: Salário recebido pelo professor.

### Tabelas de Dimensão

1. **Dimensao_Professores**: Armazena informações sobre os professores.
   - id_professor
   - nome_professor
   - titulo
   - idade

2. **Dimensao_Cursos**: Contém os dados dos cursos ministrados.
   - id_curso
   - nome_curso
   - nivel
   - duracao

3. **Dimensao_Departamentos**: Armazena os detalhes dos departamentos.
   - id_departamento
   - nome_departamento
   - chefe_departamento

4. **Dimensao_Datas**: Contém informações sobre as datas de oferta.
   - id_data
   - data
   - ano
   - mes
   - dia

## Diagrama do Star Schema

![Star Schema](./diagrama_star_schema.png)

