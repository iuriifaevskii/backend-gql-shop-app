# Install and Run

1. clone repository
2. run `npm i`
3. edit `ormconfig.json` and change your database configuration (you can also change a database type, but don't forget to install specific database driver)
4. run `npm run dev`

#### graphQL Query Example

```
query getPostsPaginate($limit: Int = 2, $offset: Int = 1) {
  posts(limit: $limit, offset: $offset) {
    count
    data {
			id
      title
      text
      categories {
        id
        name
      }
      categoryNames
    }
  }
}

mutation addPost($title: String = "first title") {
  postSave(title: $title) {
    id
    title
  }
}
```