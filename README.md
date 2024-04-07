REST-сервис на JDBC и Servlet для кулинарный рецептов. Дополнительно использовались HikariCP, Mapstruckt, Jackson. 
Для тестов использовались Junit и Mockito, дополнительно для тестирования репозитория БД использовался testcontainers.


Демонстрация работы (старая): https://youtu.be/nDYmYAnfs3g

Демонстрация работы (новая): https://youtu.be/P40mfCJdzZw

Схема БД (PostgreSQL 15):

![image](https://github.com/Kipokape/cookingRecipesRest/assets/57583013/a2348943-700d-42a9-b650-cb96efc22236)

Реализованы CRUD для всех сущностей.

Category:

 - GET http://localhost:8080/cookingRecipesRest_war_exploded/category/{id} - Запрос для получения данных категории;
 - GET http://localhost:8080/cookingRecipesRest_war_exploded/category - Запрос для получения данных всех категорий;
 - POST http://localhost:8080/cookingRecipesRest_war_exploded/category - Запрос для добавления новой категории (необходимо "name");
 - PUT http://localhost:8080/cookingRecipesRest_war_exploded/category - Запрос для изменения категории (необходимо "categoryId", "name");
 - DELETE http://localhost:8080/cookingRecipesRest_war_exploded/category/{id} - Запрос для удаления категории;


Recipe:

 - GET http://localhost:8080/cookingRecipesRest_war_exploded/recipe/{id} - Запрос для получения данных рецепта;
 - GET http://localhost:8080/cookingRecipesRest_war_exploded/recipe - Запрос для получения данных всех рецептов;
 - POST http://localhost:8080/cookingRecipesRest_war_exploded/recipe - Запрос для добавления нового рецепта (необходимо "categoryId", "name");
 - PUT http://localhost:8080/cookingRecipesRest_war_exploded/recipe - Запрос для изменения рецепта (необходимо "recipeId", "categoryId", "name");
 - DELETE http://localhost:8080/cookingRecipesRest_war_exploded/recipe/{id} - Запрос для удаления рецепта;


Ingredient:

 - GET http://localhost:8080/cookingRecipesRest_war_exploded/ingredient/{id} - Запрос для получения данных ингредиента;
 - GET http://localhost:8080/cookingRecipesRest_war_exploded/ingredient - Запрос для получения данных всех ингредиентов;
 - POST http://localhost:8080/cookingRecipesRest_war_exploded/ingredient - Запрос для добавления нового ингредиента (необходимо "name");
 - PUT http://localhost:8080/cookingRecipesRest_war_exploded/ingredient - Запрос для изменения ингредиента (необходимо "ingredientId", "name");
 - DELETE http://localhost:8080/cookingRecipesRest_war_exploded/ingredient/{id} - Запрос для удаления ингредиента;


RecipeIngredient:

 - GET http://localhost:8080/cookingRecipesRest_war_exploded/recipe-ingredient/{id} - Запрос для получения данных ингредиента рецепта;
 - GET http://localhost:8080/cookingRecipesRest_war_exploded/recipe-ingredient - Запрос для получения данных всех ингредиентов рецептов;
 - POST http://localhost:8080/cookingRecipesRest_war_exploded/recipe-ingredient - Запрос для добавления нового ингредиента рецепта (необходимо "recipeId", "ingredientId", "weight");
 - PUT http://localhost:8080/cookingRecipesRest_war_exploded/recipe-ingredient - Запрос для изменения ингредиента рецепта (необходимо "recipeIngredientsId", "recipeId", "ingredientId", "weight");
 - DELETE http://localhost:8080/cookingRecipesRest_war_exploded/recipe-ingredient/{id} - Запрос для удаления ингредиента рецепта;
