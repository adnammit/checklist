# Shopping List Name TBD

React front end with a .NET API 

## Running in Docker
just F5 it bro! current state of affairs:
* Docker .NET Launch task: gives you debugging, random port will be assigned
	{base_url}/list/e4d81920-987c-495f-85bd-2847951dbef0
* Docker .NET Launch (Compose) task: no debugging, but you get a consistent port
	http://localhost:5064/list/e4d81920-987c-495f-85bd-2847951dbef0
* note that any valid guid will do for now

## Todo
* **NEXT**
	* create boilerplate for monorepo
	* make two big decisions: backend/db/persistence, and frontend framework
	* edit item
	* delete item
* finish dockerization
	* get swagger/openapi working in docker
	* hot reloading for C#???
	* update this readme with notes about ports, urls, etc
	* add prod dockerization
		* [dockerizing react](https://www.innokrea.com/dockerizing-the-frontend-do-it-right-with-react-js-vite/)
* database
	* get db with migrations up and running
	* EF vs dbup?

