# Step by Step - Install & Configuration

## System dependencies

* PostgreSQL
* Elasticsearch
* Redis
* Ruby version 2.4.0
* Rails version 4.2.8

# Lets Get Started!

**1. Install Homebrew**
**2. Instal Ruby**
**3. Install Rails**
**4. Install PostgreSQL**
```
brew install postgresql
```
**5. Install Elasticsearch ImageMagick**
```
brew install elasticsearch
brew install imagemagick
```
Lets check it is running by visiting [http://localhost:9200](http://localhost:9200) in your browser. You should get something like this:

```
{
  name: "vIdZLoB",
  cluster_name: "elasticsearch_leslie",
  cluster_uuid: "gjNSHv2jSuO5foO-0R663w",
  version:  {
    number: "5.4.0",
    build_hash: "780f8c4",
    build_date: "2017-04-28T17:43:27.229Z",
    build_snapshot: false,
    lucene_version: "6.5.0"
  },
  tagline: "You Know, for Search"
}
```

**6. Install Redis**

Using Homebrew install Redis and then start the server:

```
brew install redis
```
**7. Clone the app**

Browse to where you want the app to live and clone app:

```
git clone https://github.com/kenny-hibino/stories.git
```

Change directory into the stories folder
```
cd stories
```


**8. Start the app**

First install all the required gems:
```
bundle install
```

Execute Sidekiq, ElasticSearch and Mailer
```
bundle exec sidekiq -q elastic search -q mailer -c 3
```

Set up and migrate the database:
```
rake db:setup
rake db:migrate
```

Create Index with elasticsearch
```
rake elasticsearch:reindex
```

Lets run the App:
```
rails server
```

Then browse to [http://localhost:3000](http://localhost:3000) to view the app in all its glory. Wait where is that “Hello World!” moment? Time to create the admin account so we can create some posts…

**9. Create an Admin account**

Enter the rails console:

```
rails console
```

Add a new user account replacing your email and password:

```
Admin.create(email: ‘your@email.com’, password: ‘password’, password_confirmation: ‘password’)
```

Close the console:

```
exit
```

Navigate to the Admin dashboard and enter your email and password:

[http://localhost:3000/admins/sign_in](http://localhost:3000/admins/sign_in)

You can now...
- Write new posts
- Feature tags by clicking on the “feature” button when on a tag pages





## Still to come - Things you may want to cover:

* Elasticsearch configuration

* OAuth configuration

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions


Please feel free to use a different markup language if you do not plan to run
<tt>rake doc:app</tt>.
