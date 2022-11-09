# Src Web Develoment v1

## เว็บไซต์นี้เขียนโดย
```js
PHP , SQL , PDO , CSS , JS
```

## Getting Started
**First, clone this Template**
<hr>

```php
git clone https://github.com/
```

### connection.php
<hr>

```php
<?php 

    $conn = mysqli_connect("localhost", "root", "", "Database");

    if (!$conn) {
        die("Failed to connec to databse " . mysqli_error($conn));
    }

?>
```

### config.php
<hr>

```php
<?php 

    $db_host = "localhost";
    $db_user = "root";
    $db_password = "";
    $db_name = "Database";

    try {
        $db = new PDO("mysql:host={$db_host}; dbname={$db_name}", $db_user, $db_password);
        $db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    } catch(PDOEXCEPTION $e) {
        $e->getMessage();
    }


?>
```

### Sql Accounts Users
<hr>

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

### Sql Stock Download
<hr>

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
