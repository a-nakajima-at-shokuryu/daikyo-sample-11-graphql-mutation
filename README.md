# daikyo-sample-11-graphql-mutation
大京のサンプル11（GraphQL更新系／Node.jsベース）

## GraphQL起動
```
> node src/data.js
```

## SELECT
```
■クエリ
query getData($id: String) {
    busho(id: $id) {
        id
        name
    }
}

■Variables
全件取得する場合、Variablesは不要
id指定で取得する場合
{
  "id": "10"
}
```

## INSERT
```
■クエリ
mutation addData($id: String! $name: String!) {
    addBusho(id: $id name: $name) {
      	id
        name
    }
}

■Variables
{
  "id": "70",
  "name": "部署Ｇ"
}
```

## UPDATE
```
■クエリ
mutation updData($id: String! $name: String!) {
    updBusho(id: $id name: $name) {
      	id
        name
    }
}

■Variables
{
  "id": "70",
  "name": "部署Ｇ＊＊＊"
}
```

## DELETE
```
■クエリ
mutation delData($id: String!) {
    delBusho(id: $id) {
        id
        name
    }
}

■Variables
{
  "id": "70"
}
```