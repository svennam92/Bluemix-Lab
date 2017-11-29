## Bluemix Watson Personality Insights Lab
See what Watson has to say about you!

### Get Started

1. Clone or [Download the zip](https://github.com/svennam92/Bluemix-Lab/archive/master.zip) file of this git repository.
1. Push your app to Bluemix
	1. Download the [Cloud Foundry CLI](https://github.com/cloudfoundry/cli#downloads) to interact with Bluemix from a terminal
		1. Direct Links: 
	[Mac](https://cli.run.pivotal.io/stable?release=macosx64&source=github) [Windows](https://cli.run.pivotal.io/stable?release=windows64&source=github)
	1. Open your terminal and `cd` to the root of your local repository's directory (Where app.js is)
	1. Run the following commands:

	```
	# Set Bluemix as your Cloud Foundry CLI target
	$ cf api api.ng.bluemix.net  
	
	# Use your Bluemix credentials to login and target an org/space
	$ cf login --sso                
	
	# Create your Watson Personality Insights service
	$ cf create-service personality_insights lite personality-insights-tutorial
		                     
	# Push your application to Bluemix
	$ cf push                    
	```	

You've just deployed your application! The manifest.yml will take care of all the extra options. When your app is done the url will show in the logs

### That's it!
Your application is now up and running in the public cloud! Go to the Bluemix application URL and write a 100 word bio about your self and click `Ask Watson`!
