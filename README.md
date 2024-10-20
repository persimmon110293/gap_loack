## How to setup
1. Clone this repository
2. Run `docker compose up -d`

## How to insert data
1. Run `docker exec -it mysql bash`
2. Run `mysql -u root -p`
3. Enter password: `root`
4. Run `use test;`
5. Run Following SQL Query:
```sql
// create table
CREATE TABLE `users` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(255) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

// insert data
INSERT INTO `users` (`id`, `name`) VALUES (10, 'Taro');
INSERT INTO `users` (`id`, `name`) VALUES (20, 'Jiro');
INSERT INTO `users` (`id`, `name`) VALUES (30, 'Saburo');
INSERT INTO `users` (`id`, `name`) VALUES (40, 'Shiro');
INSERT INTO `users` (`id`, `name`) VALUES (50, 'Goro');
```