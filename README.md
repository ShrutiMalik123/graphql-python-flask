# graphql-python-flask

# commands needed
### py -m venv env
### .\env\Scripts\activate
### pip3 install flask flask-graphql flask-migrate flask-sqlalchemy graphene graphene-sqlalchemy

# data base creation with python

### $ python
### >>> from app import db, User, Post
### >>> db.create_all()
### >>> john = User(username='johndoe')
### >>> post = Post()
### >>> post.title = "Hello World"
### >>> post.body = "This is the first post"
### >>> post.author = john
### >>> db.session.add(post)
### >>> db.session.add(john)
### >>> db.session.commit()
### >>> User.query.all()
### [<User 'johndoe'>]
### >>> Post.query.all()
### [<Post 'Hello World'>

# GraphQL query

### {
 ### allPosts{
    edges{
      node{
        title
        body
        author{
          username
        }
      }
    }
  }
}

# Mutation Query:

### mutation {
 ### createPost(username:"johndoe", title:"Hello 2", body:"Hello body 2"){
    post{
      title
      body
      author{
        username
      }
    }
  }
}

