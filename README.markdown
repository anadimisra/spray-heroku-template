## _spray_ Heroku Template Project

This projects provides a starting point for your own _spray-routing_ endeavors on Heroku, it has been forked from [spray-template](https://github.com/spray/spray-template) to add [Heroku](https://www.heroku.com) support
 
To run through sbt, follow the steps as mentioned on [spray-template](https://github.com/spray/spray-template) page. To run through foreman, follow these steps:

1. Git-clone this repository.

        $ git clone git://github.com/anadimisra/spray-heroku-template.git my-project

2. Change directory into your clone:

        $ cd my-project

3. Run the project through foreman
		
		$ foreman start
		
4. Browse to [http://localhost:5000](http://localhost:5000)

5. Learn more about hacking spray on [http://spray.io](http://spray.io)


This fork adds following changes

1. A procfile for Heroku

		$ web: target/universal/stage/bin/demo-service -Dhttp.port=$PORT -Dconfig.file=config/application.conf
		
2. An application config file to pick up environment variables when running on heroku, view the file at

		$ config/application.conf
		
3. Plugins added on top of the fork

		addSbtPlugin("com.typesafe.sbt" % "sbt-native-packager" % "1.0.0-M4")

        addSbtPlugin("com.typesafe.sbteclipse" % "sbteclipse-plugin" % "3.0.0")
      
4. Typesafe config library

		libraryDependencies += "com.typesafe" % "config" % "1.2.1"