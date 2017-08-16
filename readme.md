## Plugin db_models_daos
Plugin para code igniter 3, gera Models e DAO's para todas as tabelas de um determinado Banco de Dados.
Serve como uma camada de acesso fácil, rápido e seguro aos dados do BD.

Autor: _YagoML_

### Dependências
"Code Igniter 3":https://codeigniter.com/
"Composer":https://getcomposer.org/

- Colar a pasta application na pasta do app
- Configurar o composer, colocando na config _composer.json_ com a config do arquivo _composer_autoload.json_

### Exemplo de uso
```php
<?php
	// Busca por ID
	\DAOs\<Table>::buscarPorID($dataID);

	// Busca com filtros
	
	$filters = [];
	$filters['wheres'] = ['field' => '<field>', 'value' => <value>];
	$filters['joins'] = ['table' => '<table'>, 'field' => '<field>', 'fk' => '<f_key>'];
	$filters['orWheres'] = ['field' => '<field>', 'value' => <value>];
	$filters['order_by'] = ['field' => '<field>', 'value' => '<value>'];
	$filters['limit'] = ['start' => 0, 'qtd' => 20];
	
	\DAOs\<Table>::buscar($filters);
	
	// Inserção de Dados
	\DAOs\<Table>::inserir($dataModel);
	
	// Atualização de Dados
	\DAOs\<Table>::update($dataID, $dataModel);
	
	// Exclusão de Dados
	\DAOs\<Table>::deletar($dataID);
	
	// Quantidade de Registros
	\DAOs\<Table>::qtdRegistros();
```
