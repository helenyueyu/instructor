To instantiate a new rails project: 

`rails _5.2.3_ new FRAC --database=postgresql --skip-turbolinks`

To set up the database, we need to run: 

`bundle exec rails db:create`

To see all of our routes, we can run: 

`bundle exec rails routes`

To see all routes associated with the users controller, we can run: 

`rails routes -c user`

What is the `as:` referring to? 

Go to our `routes.rb` file and add the following: 

```rb

  get 'users', to: 'users#index'
  get 'users/:id', to: 'users#show'
  get 'users/new', to: 'users#new'
  get 'users/:id/edit', to: 'users#edit'

  post 'users', to: 'users#create'
  put 'users/:id', to: 'users#update'
  delete 'users/:id', to: 'users#destroy'

```


