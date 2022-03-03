# Padrões do banco de dados

Nomes de tabelas - PascalCase
Nomes de campos - snake_case

## Dicas de uso do SEQUELIZE

Ao criar um `model` utilize a opção `--underscored`, isso irá fazer o sequelize traduzir os campos em snake_case do banco para camelCase, assim podemos manter o padrão do JavaScript para as propriedades.

Exemplo:

```bash
npx sequelize model:generate --name <Nome-da-Model> [opções] --underscored
```

O modelo irá receber a opção `underscored: true` logo após o `modelName` e irá criar os campos `created_at` e `updated_at`;

Deve-se ter a preocupação de colocar o nome no campo em snake_case apenas na migration, e no model manter camelCase.
