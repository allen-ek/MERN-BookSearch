# MERN-BookSearch

# Authors

Allen Klein

- [Link to Portfolio Site](https://allen-ek.github.io/react-portfolio/)
- [Link to Github](https://github.com/allen-ek/react-portfolio)

# MERN Application

## Why?
I wanted to refactor older code from an api query and routes to a MERN application to using graphsql query
and mutations to store and retrive data.

## What I learned
While building this webpage I learned various React skills to build components as well as page layouts to use routes coming from Graphsql. I also learned how to manage state variables and form inputs to reflect these changes coming from the Graphsql queries. 
## Technologies Used
Github Workflow
CSS
HTML
React
Mongoose
Graphql
Javascript
## Code Snippet
```html
 const typeDefs = gql
type User {
    _id: ID
    username: String
    email: String
    bookCount: Int
    savedBooks: [Book]
}
type Auth{
    token: ID!
    user: User
}
type Book {
    bookId: String
    authors: [String]
    description: String
    title: String
    image: String
    link: String
}
input bookInput {
    bookId: String
    authors: [String]
    title: String
    description: String
    image: String
    link: String
}
type Query{
    me: User
}
type Mutation{
    login(email: String!, password: String!): Auth
    addUser(username: String!, email: String!, password: String!): Auth
    saveBook(newBook: bookInput!): User
    removeBook(bookId: ID!): User
}
  
```
The code snippet above was the code in order for graphsql to be able to store the data.

