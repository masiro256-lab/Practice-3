# Практическая работа №3. Аутентификация и роли

Каталог дополнен ASP.NET Core Identity. Учётные записи и роли хранятся в той же SQLite-базе API. Есть регистрация, вход, выход и блокировка после пяти неудачных попыток. MVC-клиент обращается к API с токеном; User читает каталог, Admin изменяет данные.

Нужен .NET 10 SDK. В первом терминале:

```powershell
dotnet restore
$env:Admin__Password = 'StudyAdmin123!'
dotnet run --project ProductCatalogApp.Api --launch-profile http
```

Во втором терминале:

```powershell
dotnet run --project ProductCatalogApp.Client --launch-profile http
```

Клиент: http://localhost:5034. Swagger: http://localhost:5100/swagger. Администратор: admin, пароль из команды выше. Зарегистрированные пользователи получают роль User.

