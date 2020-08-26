### my personal experience <br /> with software engineering hiring
ning yu



## 1
## motivation
time estimated: 20 minutes



software engineering is 
- "not important"
- "just outsource"
- "AI is the future, software is the past"


the data science "hierarchy of needs"  
<img src="https://hackernoon.com/hn-images/1*7IMev5xslc9FLxr9hHhpFw.png" width="70%">  
<small>https://hackernoon.com/the-ai-hierarchy-of-needs-18f111fcc00</small>


mastery of software is necessary for good data science  
it's not a foregone conclusion  
<img src="ds_hierarchy_software2.jpg" width="70%">



- "software developer no future one"
- "no code app development is the next big thing"
- "your company can just outsource to india/china"
- "software is so easy now, not worth your time"


the software industry isn't homogenous  
but wrapped in elitism  
you can't "farm" your way up into the trajectory


<img src="twotiers.png" width="70%">
<small><a href="http://elijames.org/the-two-tiers-of-singapores-tech-companies">http://elijames.org/the-two-tiers-of-singapores-tech-companies</a>

a lot of opinions here to consider - <a href="https://www.reddit.com/r/singapore/comments/i9d46m/two_tiers_of_tech_company_in_singapore/">recent reddit discussion</a>
</small>


my subjective, unscientific take

| higher tier   || lower tier    | 
| ------------- || ------------- | 
| software is core || software is a means to sales | 
| problems are unique, requires skill || simple problems, just need anyone to implement | 
| quality is highly valued || doesn't really matter, just get the job done | 


| higher tier || lower tier |  
| ------------- || ------------- | 
| stringent technical assessment process || hiring is done by managers/HR |
| individual empowerment || corporatised |
| (tries to be truly) agile || claims to be agile |


| higher tier || lower tier |  
| ------------- || ------------- | 
| pays well || doesn't pay well |
| technical progression || move up to management asap |
| you wanna be here || not here |



why can't you "farm" into the good places

and if you can't progress into good software roles  
how do you get in?


good software companies emphasize on technical abilities

they develop assessments that assess your current and potential skill


it's not about:
- X years of experience  
- how many degrees  
- what your job title is  

sometimes it isn't even about your previous company  
(though that actually does matter)  


it's about:
- what you have build (and can show)
- how good you are at coding
- how well you work with the team



## 2
## technical tests



some of the formats i've come across
- direct algo questions
- applied algo questions
- oop-ify something
- build a small app/api/feature

a common flow: algo -> wrap in oop -> wrap in API


mediums:
- take-home
- online 
- f2f
--- 
platforms: 
- IDE
- whiteboard
- google docs



\> whiteboarding is a terrible hiring practice

https://stackoverflow.blog/2019/12/16/this-this-whiteboard-interviews/  
(second half is satire)


my personal take
- don't see it as an excuse to not be good at technical tests
- not the sharpest tool, but still far more effective than looking at just CVs, degrees
- just a _*general name*_ for many different types of tests. some are more effective than others



<iframe width="560" height="315" src="https://www.youtube.com/embed/IWvbPIYQPFM?start=318" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


<img src="flood.png" width="70%">

given a grid of size m by n  
find the maximum number of connected colour boxes


```go
let grid be m x n array of 0
let max_count be 0
for column in m {
    for box in n {
        if grid[column][box] is 0 {
            set grid[column][box] to 1
            run dfs_by_colour on grid[column][box]
            if size is greater than max_count {
                set max_count to size
            }
        }
    }
}
 
```

```go
function dfs_by_colour {
    a basic depth (or breadth) first search to count
    set grid[][] value to 1 when it is traversed
}
```


<div style="height: 45vh"><img src="coding_interview.png"></div>

<small>Cracking the Coding Interview by Gayle Laakmann McDowell</small>



<font color=red>Given a list of movies watched by users of your app, and a movie a new user just watched, recommend another movie for him to watch.</font>  


collaborative filtering?


start simple!

find all users who also watched this movie  
and just grab the most watched movie of all these users

this is a semi-simple sql query


<font color=red>Design an app to provide an API service. The app should be able to store users, movies, watches and make recommendations.</font>


generally, this could be an MVC app.


2 models: `user`, `movie`, linked by a foreign key.

---

2 controllers: 
- user (CRUD + watch methods)
- movie (only CRUD)  

---

basic routes, plus a watch API.

---

remember to write unit tests!


<font color=red>How would you improve the performance of the recommendation API?</font>


cache results when queried, set to expire in 24 hours.

any other ideas?



## 3
## preparation



data structures and algorithms


you don't need to implement them

but you should know:
- what they are
- how they work
- how to use them
- time complexities for common operations


common operations:
- insert
- remove
- find
- next/previous


algos to know:

- recursion and dynamic programming
- basics: hashmap, array
- linear: sorts, linkedlists, deque
- nonlinear: graphs, trees, heaps


<img src="binary_tree_meme.jpg">


ways to study:
- CLRS
- take a MOOC algo class
- practice using them on leetcode



practical software engineering


OOP
- classes and instances
- inheritance
- abstract classes
- generics
- private and public
- constructors, methods and attributes
- _*this / self*_


you'll want to know how OOP is implemented in your language of choice, and what are its drawbacks! (especially interpreted languages)


fastest way to learn this: take a MOOC, and then do some exercises / build some apps



<img src="https://miro.medium.com/max/1080/0*Qf1s2lG86MjX-Zcv.jpg">


fastest way to learn this:
pick a common server framework

- ruby on rails (warning: magic)
- node/express.js
- spring (good verbosity to learn basics) 
- laravel (php if you're coming from wordpress)


I would recommend these books: [rails](https://railstutorial.org) [nodejs](https://www.manning.com/books/node-js-in-action-second-edition)


your framework may dictate where you would go. choose something you enjoy coding in. (i'm not so sure about this myself)

- banks: java (spring)
- govtech: a lot of rails evidently
- nodejs: microservices



frontend


you'll have to know javascript to do this!

pick a common frontend framework:
- react
- vuejs
- angular (?)

they're so similar, it really doesn't matter which you choose


quickly do a tutorial and understand:
- lifecycle APIs
- component props/states & other APIs
- stores, routes, mixins, etc

then, build a few apps for fun, to get used to thinking about designing apps and features.


<img src="freecodecamp.png">
<small><a href="https://www.freecodecamp.org/learn/front-end-libraries/front-end-libraries-projects/">https://www.freecodecamp.org/learn/front-end-libraries/front-end-libraries-projects/</a></small>



4. resources and tips


https://visualgo.net

website built by NUS SoC to teach students algorithms. we mug this before the exam.


https://www.leetcode.com  

great website to do some algorithm practice questions and learn algorithmic thinking


<img src="cracking_book.jpg">

world famous book on algos. has a lot of gems! every time i prep for interviews again, i go back and study this.


https://www.freecodecamp.org/learn

bunch of free stuff here. i recommend this as i've started by dev journey with this few years back.



- no one has asked me about docker, ever. docker is not a big deal imo.

- don't just learn the tool, learn the underlying concept (e.g. event loops, declarative programming)

- engineering is always about making tradeoffs

- you're not expected to know everything. feel free to ask questions, and be honest about making mistakes.

- interviews go both ways - it is also for you to assess about the company



## glhf

<img src="https://assets.bonappetit.com/photos/5ca534485e96521ff23b382b/16:9/w_2560,c_limit/chocolate-chip-cookie.jpg">



feedback
- give examples of what is a good interview vs what was a bad experience
- resources are important (compile more)
- frontend - not that important
