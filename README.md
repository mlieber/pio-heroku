# Heroku buildpack for PredictionIO Eventserver
## About
PredictionIO eventserver is an open source machine learning analytics layer for unifying events from multiple platforms. 
Refer to http://docs.prediction.io/start/ for further information.

## How to run
```
git clone https://github.com/chanlee514/pio-heroku && cd pio-heroku/
heroku create <your-eventserver-name> --buildpack=https://github.com/chanlee514/pio-heroku
heroku buildpacks:add heroku/scala
```
Request a help ticket on Heroku for slug size increase (https://help.heroku.com/tickets).
PredictionIO runs on Spark, and since Heroku currently doesn't have Spark support, 
we have to include it as part of our build. 

Commit and push to Heroku.
```
git push heroku master
```
Your eventserver will be ready at https://your-eventserver-name.herokuapp.com.
