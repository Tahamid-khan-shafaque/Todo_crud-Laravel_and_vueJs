
# Project Title

Develop a simple To-do crud module using Laravel Framework. Used VueJs for the view rendering 


## Deployment

To deploy this project need some configuration. First we will setup laravel then vue.

1.  Download ZIP from : https://github.com/Tahamid-khan-shafaque/Todo_crud-Laravel_and_vueJs.
2.  Extract the ZIP file. 
3.  Go to D or E or your prefer directory and run cmd. After that run the following commands.                     

```bash
git clone https://github.com/Tahamid-khan-shafaque/Todo_crud-Laravel_and_vueJs.git
```
```bash
cd Todo_crud-Laravel_and_vueJs
```
Go to project change the .env.example file to .env After that create a database name 
laravel_vue. Then run the following commands

```bash
php artisan key:generate
```
```bash
php artisan storage:link
```
```bash 
php artisan migrate
```
```bash
php artisan serve
```
## Vuejs setup
Don't close the php artisan serve terminal. Open another terminal in vs code and run the following command 

```bash
npm install
```

```bash
npm run dev
```
Then open this application in : http://127.0.0.1:8000


## Work flow of this Project

#### Discussion about how Laravel routes, Vue.js components, and controllers work together in this Todo List project

## Controller (app/Http/Controllers/TaskController.php):

1. `index()`: Retrieves all tasks
2. `store()`: Creates a new task
3. `update()`: Updates an existing task
4. `destroy()`: Deletes a task



## Main Component (resources/js/components/TodoList.vue):
- Contains the entire Todo List functionality.
- Uses Axios for HTTP requests to the Laravel backend.

1. `fetchTasks()`: Retrieves tasks from the backend
2. `addTask()`: Sends a POST request to create a new task
3. `updateTask()`: Sends a PUT request to update a task
4. `deleteTask()`: Sends a DELETE request to remove a task

## Data Flow:

1. Vue component makes an Axios request to a Laravel route.
2. The route directs the request to the appropriate controller method.
3. The controller interacts with the database via the `Task` model.
4. The controller returns a response, which is sent back to the Vue component.
5. The Vue component updates its state based on the response.

