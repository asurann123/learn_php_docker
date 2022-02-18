# learn_php_docker
- Build php study environment with docker
- Build PHP (including PDO, Xdebug), MySQL, phpMyAdmin environment in one shot
---

## SetUp
1. Create an appropriate directory. You can freely decide the directory name.
    - ```mkdir learn_php```

2. Clone this repository. If you add ".", It will be cloned to the current directory as it is.
    - ```git clone https://github.com/asurann123/learn_php_docker.git . ```
3. Build with docker.
    - ```docker compose up -d```
    - If you are using the old docker compose, try the command below.
    - ```docker-compose up -d```
4. Place the prepared PHP file in the src directory.
5. If you set the file in "src / hello.php", please access the following URL with your browser.
    - ```http://localhost:5050/hello.php```

---

## Specifications
1. PHP
   * Listening to "http://localhost:5050/"
   * You can debug with Xdebug.
     * Port: 9001 is listening, so after setting it as it is, open the corresponding file in the browser.
   * Since PDO is included, DB connection from PHP is also possible.
     
2. phpMyAdmin  
   * Access to phpMyAdmin is "http://localhost:4040/index.php?"
     * Login by root

3. MySQL
   * port:33006
---

## If you change docker-compose or DockerFile
- When changing the version of PHP or MySQL, etc.
1. ```docker compose build```
2. ```docker compose up -d```
