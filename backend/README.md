# Install and Run

1. clone repository
2. run `npm i`
3. edit `ormconfig.json` and change your database configuration (you can also change a database type, but don't forget to install specific database driver)
4. run `npm start`

# graphQL Query Example

query getPostsPaginate($limit: Int = 1, $offset: Int = 0) {
  posts(limit: $limit, offset: $offset) {
    id
    title
  }
}

mutation someQuery($title: String = "first title") {
  postSave(title: $title) {
    id
    title
  }
}
