### バージョン確認
```
 psql --version

```
### DBの一覧の取得
```
psql -l

```
### ユーザー/DBを指定してログイン

```

psql -U <USER_NAME> <DB_NAME>

```

### DBの切り替え

```

¥connect <DB_NAME>

```

### テーブル一覧表示

```

¥d

```

### スキーマ作成

```

create schema <SCHEMA_NAME> AUTHORIZATION <USER_NAME>

```

### スキーマ一覧表示

```

\dn

```

### 現在のスキーマの確認

```

select current_schema();

```

### スキーマの変更

```

set search_path = <SCHEMA_NAME>;

```
