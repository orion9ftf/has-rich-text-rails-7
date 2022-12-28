### has_rich_text

1.- Create app

```shell
$ rails new app-test
```

2.- Create scaffold

```shell
$ rails g scaffold post title
```

3.- Install rich_text

```shell
$ rails g action_text:install
```

4.- Migrate

```shell
$ rails db:migrate
```

5.- Add body in strongs params

```rb
def post_params
  params.require(:post).permit(:title, :body)
end
```

6.- Add has_rich_text in post model

```rb
  has_rich_text :body
```


