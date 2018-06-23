# After-workshop Go exercises #T3DD18

## Basic data structures

### DS-1 - Create a Node data type

Let's create a node datatype, with following fields :

* UUID
* PUUID (UUID of the parent node)
* Title

#### Ressources

* https://github.com/google/uuid

## Tree operations

### TR-1 - Create a tree of Nodes

Create programmatically an hierarchical, non looped tree of Nodes, with at least 3 level of depth. The tree should contain at least 3 Nodes on each level.

* https://tour.golang.org/flowcontrol/1
* https://github.com/drhodes/golorem

### TR-2 - Search a Node by it's title, return the UUID

Create programmatically an hierarchical, non looped tree of Nodes, with 3 level of depth. The tree should contain at least 10 Nodes.

* https://stackoverflow.com/questions/1841443/iterating-over-all-the-keys-of-a-map
* https://stackoverflow.com/questions/28495679/iterate-struct-map-key-value-in-golang


## Database operations

### DB-1 - Create a SQLite database and table

Create a SQLite database and nodes table, with uuid, puuid, title. 

#### Ressources

* https://github.com/mattn/go-sqlite3
* https://stackoverflow.com/questions/4098008/create-table-in-sqlite-only-if-it-doesnt-exist-already

### DB-2 - Basic CRUD operations with SQL

* Insert nodes into the database
* Select and print UUIDs and titles of nodes
* Update a title of a node by it's UUID
* Remove a node by UUID

#### Ressources

* https://astaxie.gitbooks.io/build-web-application-with-golang/en/05.3.html

### DB-3 - CRUD with ORM

* Insert nodes into the database with GORM
* Select and print UUIDs and titles of nodes with GORM
* Update a title of a node by it's UUID with GORM
* Remove a node by UUID with GORM

#### Ressources

* http://doc.gorm.io/models.html#model-definition
* http://doc.gorm.io/crud.html#create
* https://github.com/jinzhu/gorm
* https://github.com/insionng/zenpress/blob/master/model/post.go

## JSON encode / decode

### JO-1 - JSON encode 

Add additional JSON descriptors to Your Node structure.
Read all nodes from Your database.
Encode it into a JSON, print it in the terminal.

* https://gobyexample.com/json
* https://golang.org/pkg/encoding/json/

### JO-2 - JSON decode

Decode encoded JSON string from JO-1 exercise, print only titles of each node, one by line.

## Files operations

### FS-1 - Write a file 

Read all nodes from Your database, and create a JSON file `nodes.json`.

* https://gobyexample.com/writing-files
* https://golang.org/pkg/io/ioutil/

### FS-2 - Read a file 

Read the content of the file and show it's content in the terminal.

* https://gobyexample.com/reading-files

## HTTP server

### HT-1 - Create a simple HTTP server 

Create a simple HTTP server, which will listen on port 3000.
Output "Hello T3DD18!" on every connect.

* https://github.com/go-chi/chi
* https://github.com/go-chi/chi/blob/master/_examples/hello-world/main.go

## REST interface

### RS-1 - List nodes via REST

On each GET request http://localhost/nodes, list all nodes from Your database.

* https://github.com/go-chi/chi/blob/master/_examples/rest/main.go#L83

### RS-2 - Create a node via REST

On each POST request http://localhost/nodes, create a node in the database.

* https://github.com/go-chi/chi/blob/master/_examples/rest/main.go#L84

### RS-3 - REST single node operations

#### RS-3-1 - Node creation

On each GET request http://localhost/nodes/UUID, create a node in the database and show it's UUID in the browser.

* https://github.com/go-chi/chi/blob/master/_examples/rest/main.go#L89

#### RS-3-2 - Node update

On each PUT request http://localhost/nodes/UUID, update the title of the node by it's UUID in the database.

* https://github.com/go-chi/chi/blob/master/_examples/rest/main.go#L90

#### RS-3-2 - Node delete

On each DELETE request http://localhost/nodes/UUID, delete a selected node in the database.

* https://github.com/go-chi/chi/blob/master/_examples/rest/main.go#L91

## Caching

### CH-1 - Cache implementing

Implement in-memory key:value Go cache with 5 minutes expiration for nodes listing GET request.

* https://github.com/patrickmn/go-cache

### CH-2 Additional middleware cache

Add a cache for GET request for nodes listing.

* https://github.com/go-chi/httpcoala

## Advanced content types

### Exercise CT-1 - Article

Create a `model/article.go` with fields, which will be needed to represent an Article.

* https://tour.golang.org/moretypes/2
* https://github.com/dionyself/golang-cms/blob/master/models/article.go
* https://golang.org/doc/effective_go.html?#embedding
* https://schema.org/Article


### Exercise CT-2 - Place

Create a `model/place.go` with fields, which will be needed to represent a Place.

* https://schema.org/Place

### Exercise CT-3 - Event

Create a `model/event.go` with fields, which will be needed to represent a Place.

* https://schema.org/Event

## ACL

TBD

## Templating

TBD

## Themes

TBD

## Sessions handling

TBD

## WYSIWYG data processing

TBD

## Backend interface

TBD
