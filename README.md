# Laravel Application Creator (ARM64)

1. Initialize Laravel project
```shell
docker-compose run --rm composer create-project --prefer-dist laravel/laravel <project_folder_path>
```

2. Update .env file in your new application (these properties were also set in ./env/mysql.env)
```properties
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret
```

3. Run containers
```shell
docker-compose up -d --build server php mysql
```

4. Run migrations
```shell
docker-compose run --rm artisan migrate
```

5. Now you can access your application on `localhost:8000`
