 is a query language and server-side runtime for APIs that prioritizes giving clients exactly the data they request and no more

## Concepts
Let's briefly discuss some key concepts in GraphQL:
* ### ***Schema**
	* A GraphQL schema describes the functionality clients can utilize once they connect to the GraphQL server.
* ### ***Queries**
	* A  query is a request made by the client. It can consist of fields and arguments for the query. The operation type of a query can also be a [mutation](https://graphql.org/learn/queries/#mutations) which provides a way to modify server-side data.
* ### ***Resolvers**
	* Resolver is a collection of functions that generate responses for a GraphQL query. In simple terms, a resolver acts as a GraphQL query handler.

# How is it same/different from REST
* Both send HTTP request and receive HTTP responses
* REST centers around resources each identified by a URL
* GraphQL we specify the exact resources we need and fields we want
* Disadvantages 
	* REST can be called by curl or web browser
	* In graph we need heavier tooling support, both on client and server
	* Hard to cache, http has a well defined cache 
		* single point of entry uses http post by default prevents caching
		* extra work to get cache

