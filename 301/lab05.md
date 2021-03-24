# Heroku: Introduction to Node.js:
Heroku is a container-based cloud Platform as a Service (PaaS). Developers use Heroku to deploy, manage, and scale modern apps. It is flexible, and easy to use, offering developers the simplest path to getting their apps to market. Heroku is a cloud platform as a service (PaaS) supporting several programming languages. One of the first cloud platforms, Heroku has been in development since June 2007, when it supported only the Ruby programming language, but now supports Java, Node.js, Scala, Clojure, Python, PHP, and Go. For this reason, Heroku is said to be a polyglot platform as it has features for a developer to build, run and scale applications in a similar manner across most languages.

Steps for setting up Heruko for Node.js:

1.Install Heruko.

2.Preparing the Heruko app.

3.Deploying the app.

4.View logs.

5.Define a Procfile, which is a text file in the root directory of your application, to explicitly declare what command should be executed to start your app. web: node index.js This declares a single process type, web, and the command needed to run it. The name web is important here. It declares that this process type will be attached to the HTTP routing stack of Heroku, and receive web traffic when deployed.

6.Scale the app.

7.Declare app dependencies.

8.Run the app locally.

9.Push local changes.

10.Add addons.

11.Start working!