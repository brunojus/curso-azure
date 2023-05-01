

## Resources

- http://localhost:8000/currency-exchange/from/USD/to/BRL

```json
{
  "id": 10001,
  "from": "USD",
  "to": "BRL",
  "conversionMultiple": 5.05,
  "environmentInfo": "NA"
}
```

## H2 Console

- http://localhost:8000/h2-console
- Use `jdbc:h2:mem:testdb` as JDBC URL


## Notes

## Tables Created
```
create table exchange_value 
(
	id bigint not null, 
	conversion_multiple decimal(19,2), 
	currency_from varchar(255), 
	currency_to varchar(255), 
	primary key (id)
)
```

### Creating Container

- docker build -t curso:1.0 .

### Running Container

#### Basic
```
docker run -d -p 8000:8000 --name webserver curso:1.0
```
