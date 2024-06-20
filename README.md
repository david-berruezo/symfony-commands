# symfony-commands

### SYMFONY SIMPLE COMMANDS
### -------------------------------

### LISTAR TODOS LOS COMANDOS
### ----------------------------------------------------------------------
#### php bin/console


### LISTAR TODOS LOS COMANDOS DOCTRINE
### ----------------------------------------------------------------------
#### php bin/console list doctrine 


### Symfony
### -------------------------------------------------------------------------
#### 01.- INSTALAR EL INSTALADOR
#### 01.1.- https://github.com/symfony/symfony-installer
#### 01.2.- php -r "file_put_contents('symfony', file_get_contents('https://symfony.com/installer'));"
#### 02.- COMPOSER INIT



### CREAR UNA APLICACIÓN VACIA SKELETON CON LO MINIMO | OTRA APLICACIÓN DEMO
### -------------------------------------------------------------------------
#### composer create-project symfony/skeleton pisosenmanresa


### CREAR UNA APLICACIÓN VACIA WEBSITE
### --------------------------------------------------------------------------
#### composer create-project symfony/website-skeleton pisosenmanresa


### BORRAR CACHE
### -------------------------------------------------
#### php bin/console doctrine:schema:validate							(para validar la base de datos)
#### php bin/console doctrine:schema:drop --force					(borrar cualquier esquema)
#### php bin/console doctrine:schema:create							(crear un nuevo esquema)
#### php bin/console doctrine:schema:update --force					(actualizar el esquema)
#### php bin/console doctrine:schema:update --force --dump-sql		(actualizar la base de datos)	

#### php bin/console doctrine:cache:clear-metadata
#### php bin/console doctrine:cache:clear-query
#### php bin/console doctrine:cache:clear-result

#### php bin/console   cache:clear                             Clears the cache
#### php bin/console   cache:pool:clear                        Clears cache pools
#### php bin/console   cache:warmup                            Warms up an empty cache
#### php bin/console   doctrine:cache:clear-collection-region  Clear a second-level cache collection region.
#### php bin/console   doctrine:cache:clear-entity-region      Clear a second-level cache entity region.
#### php bin/console   doctrine:cache:clear-metadata           Clears all metadata cache for an entity manager
#### php bin/console   doctrine:cache:clear-query              Clears all query cache for an entity manager
#### php bin/console   doctrine:cache:clear-query-region       Clear a second-level cache query region.
#### php bin/console   doctrine:cache:clear-result             Clears result cache for an entity manager



### SYMFONY MAKER BUNDLE
### -------------------------------------------------------------------------
#### Symfony 6.1.12 (env: dev, debug: true) #StandWithUkraine https://sf.to/ukraine

#### Usage:
#### command [options] [arguments]

#### Options:
####  -h, --help            Display help for the given command. When no command is given display help for the list command
####  -q, --quiet           Do not output any message
####  -V, --version         Display this application version
####      --ansi|--no-ansi  Force (or disable --no-ansi) ANSI output
####  -n, --no-interaction  Do not ask any interactive question
####  -e, --env=ENV         The Environment name. [default: "dev"]
####      --no-debug        Switch off debug mode.
####  -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug

#### Available commands for the "make" namespace:
####   make:auth                   Creates a Guard authenticator of different flavors
####   make:command                Creates a new console command class
####   make:controller             Creates a new controller class
####   make:crud                   Creates CRUD for Doctrine entity class
####   make:docker:database        Adds a database container to your docker-compose.yaml file
####   make:entity                 Creates or updates a Doctrine entity class, and optionally an API Platform resource
####   make:fixtures               Creates a new class to load Doctrine fixtures
####   make:form                   Creates a new form class
####   make:functional-test        Creates a new test class
####   make:message                Creates a new message and handler
####   make:messenger-middleware   Creates a new messenger middleware
####   make:migration              Creates a new migration based on database changes
####   make:registration-form      Creates a new registration form system
####   make:reset-password         Create controller, entity, and repositories for use with symfonycasts/reset-password-bundle
####   make:security:form-login    Generate the code needed for the form_login authenticator
####   make:serializer:encoder     Creates a new serializer encoder class
####   make:serializer:normalizer  Creates a new serializer normalizer class
####   make:stimulus-controller    Creates a new Stimulus controller
####   make:subscriber             Creates a new event subscriber class
####   make:test                   [make:unit-test|make:functional-test] Creates a new test class
####   make:twig-component         Creates a twig (or live) component
####   make:twig-extension         Creates a new Twig extension with its runtime class
####   make:unit-test              Creates a new test class
####   make:user                   Creates a new security user class
####   make:validator              Creates a new validator and constraint class
####   make:voter                  Creates a new security voter class



### DATA FIXTURES
### -------------------------------------------------------------------------
#### composer require --dev orm-fixtures
#### bin/console doctrine:fixtures:load


### CREAR REPOSITORIOS DIRECTAMENTE
### -------------------------------------------------------------------------
#### 01.- php bin/console doctrine:mapping:import "App\Entity" annotation --path=src/Entity --force
#### 02.- @ORM\Entity(repositoryClass=App\RepositoryNuevo\DynamicGeolocalityRepository::class) (COPIAR EN LA ENTIDAD PARA QUE CREE LOS REOPISOTRIOS EN EL DIRECTORIO DE LA ENTIDAD)
#### 03.- php bin/console make:entity --regenerate App\\Entity --overwrite			  (COPIAR LOS REPOSITORIOS DEL DIRECTORIOS DE LA ENTIDAD A LA CARPETA REPOSITORY)
#### 04.- renombrear RepositoryNuevo por Repository
#### 05.- la frase ORIGINAL ES: 
#### 	@ORM\Entity(repositoryClass=DynamicGeolocalityRepository::class)
#### 	@ORM\Entity(repositoryClass=LanguagesRepository::class)



### COMANDOS DOCTRINE DENTRO DE SYMFONY
### -------------------------------------------------
#### 00.- php bin/console doctrine:schema:validate
#### 01.- php bin/console doctrine:schema:drop --force 
#### 02.- php bin/console doctrine:schema:create
#### 03.- php bin/console doctrine:schema:update --force
#### 04.- php bin/console doctrine:schema:update --force --dump-sql
#### 05.- php bin/console doctrine:mapping:import "App\Entity" annotation --path=src/Entity --force
#### 06.- php bin/console make:entity --regenerate App 


### MIGRATIONS
### ----------------------------------------------------------------------
#### php bin/console make:migration
#### php bin/console doctrine:migrations:migrate

#### php bin/console doctrine:migrations:current                 [current] Outputs the current version.
#### php bin/console doctrine:migrations:diff                    [diff] Generate a migration by comparing your current database to your mapping information.
#### php bin/console doctrine:migrations:dump-schema             [dump-schema] Dump the schema for your database to a migration.
#### php bin/console doctrine:migrations:execute                 [execute] Execute a single migration version up or down manually.
#### php bin/console doctrine:migrations:generate                [generate] Generate a blank migration class.
#### php bin/console  doctrine:migrations:latest                 [latest] Outputs the latest version number
#### php bin/console  doctrine:migrations:migrate                [migrate] Execute a migration to a specified version or the latest available version.
#### php bin/console  doctrine:migrations:rollup                 [rollup] Roll migrations up by deleting all tracked versions and inserting the one version that exists.
#### php bin/console  doctrine:migrations:status                 [status] View the status of a set of migrations.
#### php bin/console  doctrine:migrations:up-to-date             [up-to-date] Tells you if your schema is up-to-date.
#### php bin/console  doctrine:migrations:version                [version] Manually add and delete migration versions from the version table.
#### php bin/console  doctrine:migrations:sync-metadata-storage  [sync-metadata-storage] Ensures that the metadata storage is at the latest version.
#### php bin/console  doctrine:migrations:list                   [list-migrations] Display a list of all available migrations and their status.
