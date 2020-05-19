<!-- .slide: data-background="/images/slide1.png" data-background-size="100% 100%"-->


# Data Analytics

### My Journey

![corona](/images/journey_tech_woman_t.png)<!-- .element  width="30%" -->

--

## About Me



<small>
<div id="container">
  <div id="navbar" class="column1">
    <ul>
       <li >Software Engineer & Data Scientist</li>
       <li >CTO & instructor at CodeOp</li>
       <li >Founder EarthPulse</li>
       <li >Reviewer for the H2020 European Research and Innovation Programmes</li>
       <li >FOSS enthusiast, Charter member OSGeo</li>
    </ul>
  </div>
    <div id="content" class="column2">
    <img src="https://raw.githubusercontent.com/doublebyte1/keynotes/master/assets/pasta_fresca.jpg" >
  </div>
</div>

</small>

---

## PhD @UCL
Geospatial analysis, network analysis
<table style="border-collapse: collapse; color:white; border: 0px yellow solid">
    <tr>
        <td></td>
        <td></td>
        <td><img src="/images/gandhi.jpg" height="30%" style="background:none; border:none; box-shadow:none;"></td> 
        <td><img src="/images/coldplay.png" height="30%" style="background:none; border:none; box-shadow:none;"></td>
    </tr>
    <tr>
        <td><img src="/images/spmod.gif" height="200px" style="background:none; border:none; box-shadow:none;"></td> 
        <td><img src="/images/spemod1.png" height="200px" style="background:none; border:none; box-shadow:none;"></td>
        <td><img src="/images/spemod2.png" height="200px" style="background:none; border:none; box-shadow:none;"></td>
        <td><img src="/images/spemod3.png" height="200px" style="background:none; border:none; box-shadow:none;"></td>
    </tr>    
</table>

--
## What is Data Analytics?

- Science of analyzing raw data in order to make conclusions about that information.<!-- .element: class="fragment" -->
- Can reveal trends and metrics that would otherwise be lost in the mass of information.<!-- .element: class="fragment" -->
- Any type of information can be subjected to data analytics techniques to get insight that can be used to improve things.<!-- .element: class="fragment" -->

---
## Data Analytics have been around for a very long time

![corona](/images/Ancientlibraryalex.jpg)<!-- .element  width="40%" -->

---
## Broad Street cholera outbreak 


- 1846–1860 cholera pandemic 
- Killed 616 people
- Miasma theory 

---
## John Snow’s Investigation

<div id="container">
  <div id="navbar" class="column1">
    <ul>
Snow hypothesized that cholera was spread by an agent in contaminated water.
  </div>
    <div id="content" class="column2">
    <img src="/images/john_snow_crossed.png">
  </div>
</div>


--

![corona](/images/snow_map.png)

--

## WTF is Heroku?

[https://www.heroku.com/](https://www.heroku.com/)

- Polyglot cloud platform as a service.<!-- .element: class="fragment" -->
- Supports several programming languages.<!-- .element: class="fragment" -->
- Runs applications in virtual containers.<!-- .element: class="fragment" -->
- Supports diverse databases.<!-- .element: class="fragment" -->


Note:
- Free tier ($$).
- Easy to use: it works a bit like git
--
## Example?

[https://leaflet-react.herokuapp.com/](https://leaflet-react.herokuapp.com/)
![corona](/images/leaflet_heroku.png)<!-- .element  width="80%" -->

Note:
- Notice the url structure
--
## Easy to use
![corona](/images/child1.jpeg)<!-- .element  width="40%" -->

--
## Deploy in 5 easy Steps
1. Register <!-- .element  style="color:red" -->
2. Install heroku-cli  <!-- .element  style="color:red" -->
2. Login <!-- .element  style="color:blue" -->
- Add remote hook <!-- .element  style="color:blue" -->
- Push code <!-- .element  style="color:green" -->

---
## Register
![corona](/images/heroku_register.png)<!-- .element  width="80%" -->

Note:
- Register for a free account

---
## Install heroku-cli

[https://devcenter.heroku.com/articles/heroku-cli](https://devcenter.heroku.com/articles/heroku-cli)

Ubuntu:
```bash
sudo snap install --classic heroku
```
macOS:
```bash
brew tap heroku/brew && brew install heroku
```

Note:
- Register for a free account

---

## Login

```bash
heroku login
```

Note:
- It authenticates with the Heroku page
---
## Add remote hook

```bash
heroku create
```

---
## Push code

```bash
git push heroku master
```

--
## Open application

```bash
heroku open
```
Note:
- Et voila! go to your browser and open the page
- DB is missing: checking the logs

--
## Checking the logs

```bash
heroku logs --tail
```
Note:
- This is the equivalent to viewing the terminal
--
## mLab

[https://elements.heroku.com/addons/mongolab](https://elements.heroku.com/addons/mongolab)
- Mongo database as a service.<!-- .element: class="fragment" -->
- web-based management tools.<!-- .element: class="fragment" -->
- Runs on a AWS EC2.<!-- .element: class="fragment" -->


Note:
- Managed mongodb database
- free tier

---
## mLab how-to

- Install add-on
- Attach to application
- get db uri and add it to your application:

```bash
heroku config:get MONGODB_URI
```

Note:
- Et voila! Open the application
- Try firefox or postman

--
## A couple things more

Note:
- Advanced topics

--
## I hate this url!

[https://dashboard.heroku.com/apps](https://dashboard.heroku.com/apps)

- Settings -> App Name
- **Update git remotes**

```bash
git remote rm heroku
heroku git:remote -a newname
```

Note:
- just add the app name! not the complete url

--
## Keep the mongo uri private
- Can we use a .env file?<!-- .element: class="fragcment" -->
- Environment variables on heroku<!-- .element: class="fragment" -->


```bash
heroku config:set SOME_NAME=mongodb://heroku_91trhphh:2s7ibta8l5ukocvbjl120hr9@ds263638.mlab.com:63638/heroku_91trhphh
heroku config:get SOME_NAME
```
<!-- .element: class="fragment" -->

Note:
- The answer is "no", we cannot use a .env file. But we can use environment variables
- - Settings config vars: we can use the dashboard or the command line
- process.env.DATABASE_URL

--
## Access MLAB Dashboard

```bash
heroku addons:open mongolab
```
Note:
- Open on the browser
- you can do ultiple things, such as query or remove your collectins
- you can also access the db via command line

--
## Have fun!
![corona](/images/child2.jpeg)<!-- .element  width="40%" -->

--

This presentation was created using [Reveal.js](https://revealjs.com/#/), the HTML presentation framework. Fork it at:
[ https://github.com/CodeOp-tech/heroku]( https://github.com/CodeOp-tech/heroku)

```
npx reveal.js-online
```

</small>


