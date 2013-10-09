---
layout: post
title: "Some Rails Basics"
description: ""
category: 
tags: []
---
{% include JB/setup %}

I've been working through the second class of the Tealeaf program (Rapid Prototyping with Ruby on Rails) for a week now. It has been, in a word, a whirlwind! I've been messing around with Rails for about 9 months prior to enrolling in the Tealeaf Program, but I can't believe how quickly I'm learning all sorts of different things about Rails and web development in general. 

As part of our first week we've been given a 15 question quiz on some Rails and web development basics. I thought this would be a perfect thing to include here in case others ever have similar questions. 

<!-- more -->

1. Why do they call it a relational database?

    - A relational database involves a series of tables with primary keys and foreign keys that map relationships between the tables. For example, lets say you have two tables: Users and Posts. The "users" table would consist of columns such as "username" and "created_at" as well as an "id" column and would be filled in with rows of different users. Almost every table will have an "id" column referred to as that table's primary key. The "posts" table would have columns like "title" and "description" in addition to the "id" column. Each row in the "post" table would be filled with a post's information. How would we know which user wrote a post? The "posts" table would also include a column titled "user_id". This "user_id" would be the foreign key of the "posts" table and would correspond to the primary key ("id") of the "users" table. That's the "relational" part in "relational database". The relationship is set up with two simple pieces of code in the User and Post controllers.

		{% highlight ruby %}

		class User < ActiveRecord::Base
		  has_many :posts
		end

		{% end %}

		{% highlight ruby %}

		class Post < ActiveRecord::Base
		  belongs_to :user
		end

		{% end %}

2. What is SQL?

    - SQL stands for Structured Query Language and is a language designed to communicate with and change databases

3. There are two predominant views into a relational database. What are they, and how are they different?

    - The two types of views are read-only and updateable. The primary difference is whether or not the database system can perform reverse mapping between the view and database schema. If it can, then it is updateable. Otherwise, the view is read-only.

4. In a table, what do we call the column that serves as the main identifier for a row of data? We're looking for the general database term, not the column name.
5. What is a foreign key, and how is it used?
6. At a high level, describe the ActiveRecord pattern. This has nothing to do with Rails, but the actual pattern that ActiveRecord uses to perform its ORM duties.
7. If there's an ActiveRecord model called "CrazyMonkey", what should the table name be?
8. If I'm building a 1:M association between Project and Issue, what will the model associations and foreign key be?
9. Given this code
class Zoo
  has_many :animals
end
    - What do you expect the other model to be and what does database schema look like?
    - What are the methods that are now available to a zoo to call related to animals?
    - How do I create an animal called "jumpster" in a zoo called "San Diego Zoo"?
10. What is mass assignment? What's the non-mass assignment way of setting values?
11. What does this code do? Animal.first
12. If I have a table called "animals" with columns called "name", and a model called Animal, how do I instantiate an animal object with name set to "Joe". Which methods makes sure it saves to the database?
13. How does a M:M association work at the database level?
14. What are the two ways to support a M:M association at the ActiveRecord model level? Pros and cons of each approach?
15. Suppose we have a User model and a Group model, and we have a M:M association all set up. How do we associate the two?
