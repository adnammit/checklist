# Shopping Time! 💅

I couldn't find a shopping app that I like for a price that I was willing to pay, so I made my own

[let's go shopping](https://shop.amandaryman.com/list)

Multirepo using git submodules and docker-compose:
* Client: React + TypeScript + Vite
* API: ASP.NET Core + Entity Framework
* DB: PostgreSQL

## Getting Started
* clone this repo using `--recurse` to get the submodules
* for db setup, you will need to create an `.env` file in the root of the project with the following variables:
	```
		POSTGRES_USER=
		POSTGRES_PASSWORD=
		POSTGRES_HOST=
		POSTGRES_DB=
	```
* launch the vscode task "Whole Enchilada"
	* builds all containers with `docker-compose`
	* attaches the debugger to the API
	* hot-reloading for the React app
* [client url](localhost:3000)
* [service url](localhost:5064) 
	* [default test endpoint](http://localhost:5064/test)
	* [list items url](http://localhost:5064/list)
* [db url](localhost:5433)
* [metabase](localhost:3030) (not working yet)
* open api and swagger (not working yet)

## Production
* [client](https://shop.amandaryman.com/list/)

## Todo
* **NEXT**
	* prod deployments
	* [dbup and dapper](https://medium.com/cheranga/database-migrations-using-dbup-in-an-asp-net-core-web-api-application-c24ccfe0cb43)
	* metabase y u no?
	* create boilerplate for multirepo
	* make two big decisions: backend/db/persistence, and frontend framework
	* edit item
	* delete item
* finish dockerization
	* get swagger/openapi working in docker
	* hot reloading for C#???
	* update this readme with notes about ports, urls, etc
	* add prod dockerization
		* [dockerizing react](https://www.innokrea.com/dockerizing-the-frontend-do-it-right-with-react-js-vite/)
		* [dockerizing .NET](https://learn.microsoft.com/en-us/dotnet/core/docker/build-container)
* database
	* get db with migrations up and running
	* serial vs uuid for pk
	* [dbup](https://github.com/DbUp/DbUp)
	* [EF vs Dapper](https://youtu.be/7ZcbHFmgVAI?si=8_YyrjMR3TzqQM9s)
* client
	* add husky pre-commit hooks for prettier and eslint
