*  divides an application into logical layers and physical tiers
* Layers are a way to separate responsibilities and manage dependencies
* A higher layer can use services in a lower layer, but not the other way around
* Tiers are physically separated, running on separate machines
*  Several layers might be hosted on the same tier

## Can be two types
- In a closed layer architecture, a layer can only call the next layer immediately down.
- In an open layer architecture, a layer can call any of the layers below it.

## 3-Tier 
- **Presentation layer**: Handles user interactions with the application.
- **Business Logic layer**: Accepts the data from the application layer, validates it as per business logic and passes it to the data layer.
- **Data Access layer**: Receives the data from the business layer and performs the necessary operation on the database.

## 2-Tier
In this architecture, the presentation layer runs on the client and communicates with a data store. There is no business logic layer or immediate layer between client and server.

## 1-Tier
It is the simplest one as it is equivalent to running the application on a personal computer. All of the required components for an application to run are on a single application or server.