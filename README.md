# CIDADES_ESTADOS_IBGE
SQL com Estados, Cidades, Distritos e Sub-Distritos com seus códigos IBGE

Após executar o sql em seu banco você pode obter os dados da seguinte forma:

### Consultar cidade por UF

```sql
SELECT * FROM cidades_estados WHERE uf_sigla LIKE 'PR';
```

O seu retorno será uma view desta forma:

| cidade\_codigo\_ibge | cidade\_nome | uf\_codigo\_ibge | uf\_nome | uf\_sigla |
| :--- | :--- | :--- | :--- | :--- |
| 4115200 | Maringá | 41 | Paraná | PR |

### Consultar distrito por cidade:

```sql
SELECT * FROM distritos_cidades_estados WHERE cidade_nome LIKE 'Toledo';
```

O seu retorno será uma view desta forma:

| distrito\_codigo\_ibge | distrito\_nome | cidade\_codigo\_ibge | cidade\_nome | uf\_codigo\_ibge | uf\_nome | uf\_sigla |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 316910905 | Toledo | 3169109 | Toledo | 31 | Minas Gerais | MG |
| 412770008 | Concórdia do Oeste | 4127700 | Toledo | 41 | Paraná | PR |
| 412770010 | Dez de Maio | 4127700 | Toledo | 41 | Paraná | PR |
| 412770015 | Dois Irmãos | 4127700 | Toledo | 41 | Paraná | PR |
| 412770020 | Novo Sarandi | 4127700 | Toledo | 41 | Paraná | PR |
| 412770040 | Novo Sobradinho | 4127700 | Toledo | 41 | Paraná | PR |
| 412770025 | São Luiz do Oeste | 4127700 | Toledo | 41 | Paraná | PR |
| 412770030 | São Miguel | 4127700 | Toledo | 41 | Paraná | PR |
| 412770005 | Toledo | 4127700 | Toledo | 41 | Paraná | PR |
| 412770033 | Vila Ipiranga | 4127700 | Toledo | 41 | Paraná | PR |
| 412770035 | Vila Nova | 4127700 | Toledo | 41 | Paraná | PR |

### Consultar subdistrito por cidade:

```sql
SELECT * FROM sub_distritos_cidades_estados WHERE cidade_nome LIKE 'Curitiba';
```

O seu retorno será uma view desta forma:

| subdistrito\_codigo\_ibge | subdistrito\_nome | distrito\_codigo\_ibge | distrito\_nome | cidade\_codigo\_ibge | cidade\_nome | uf\_codigo\_ibge | uf\_nome | uf\_sigla |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 41069020507 | Administração Regional Pinheirinho | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020504 | Administração Regional da Boa Vista | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020509 | Administração Regional da Cidade Industrial de Curitiba | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020501 | Administração Regional da Matriz | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020505 | Administração Regional de Santa Felicidade | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020508 | Administração Regional do Bairro Novo | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020502 | Administração Regional do Boqueirão | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020503 | Administração Regional do Cajuru | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020506 | Administração Regional do Portão | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
| 41069020510 | Administração Regional do Tatuquara | 410690205 | Curitiba | 4106902 | Curitiba | 41 | Paraná | PR |
