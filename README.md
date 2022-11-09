# Src Web Develoment

## Getting Started
**First, clone this Template**
```php
git clone https://github.com/
```

### DataBase
```sql
CREATE TABLE accounts (
    id INT(5) NOT NULL PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(200) NOT NULL,
    firstname VARCHAR(100) NOT NULL,
    lastname VARCHAR(100) NOT NULL,
    gmail VARCHAR(100) NOT NULL,
    class enum('member','admin') NOT NULL DEFAULT 'member'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

```sql
CREATE TABLE stock (
    id INT(5) NOT NULL PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) NOT NULL,
    description VARCHAR(100) NOT NULL,
    price VARCHAR(100) NOT NULL,
    image VARCHAR(100) NOT NULL,
    contact VARCHAR(100) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```
