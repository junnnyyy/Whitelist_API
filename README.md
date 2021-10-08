# Whitelist_API

This project is only experimental, use carefully. Im not responsible for any fatal errors for any project.
Always use on testnet before using on mainnet
This project works offchain and does not validate whitelisted users using on chain data !
This repo is intended to be used with Candy Machine Mint site, or with my repo Candy_Machine_Whitelist_Site


##How to run:
Clone the repo (obviously)

### 1) Install dependencies using 
```yarn install```

### 2) Add your own environmental variables (.env)
```
SECRET_KEY=__MY_KEY__
```
Your API authentication key used to prevent someone else from accessing the api and updating whitelisted users
#### after you are done rename ".env.sample" to ".env"


### 3) create a csv containing the list of whitelisted users and reserves for each user

#### REQUIREMENTS FOR CSV FILE:
1) Must be comma delimted
2) Must have two Columns: 1)member 2)reserve , Its important to name the two columns exactly like this
```
each row has a member which is the address of the user you wish to whitelist, reserve is how many nfts can they this address mint
```
3) Must be named whitelisted.csv
4) Must be in the main directory, do not put in a seperate file called assets or similar.
    

### 4) Edit the config.json to your needs
#### To reload the csv list everytime the script runs
```set load_csv_onetime = false```
#### If you wish to run the script once and not have it run everytime
	```
	set load_csv_one time = true
	and loaded = false
	```



### 5) Upload to a hosting server, we recommend heroku. if you decide to use heroku here are the steps to setting that up:
if you prefer tutorials, this one is good and features two options: https://www.youtube.com/watch?v=Rz886HkV1j4&t=733s
#### IMPORTANT: MAKE SURE TO FOLLOW THE STEPS FOR ADDING .ENV TO THE HOSTING SYSTEM (included in the video)
#### ALL COMMANDS SHOULD BE RAN IN THE MAIN DIRECTORY 
Install the heroku CLI: https://devcenter.heroku.com/articles/heroku-cli
1. run: ```heroku login``` , and then login into your account.
2. run ```git init```
3. run ```heroku git:remote -a Name_Of_Your_Project```
4. run ```git add .```
5. run ```git commit -m "first-commit```
6. run ```git push heroku master``` heroku will then supply you with two urls, one of which is the url of the API, the other is not important (the one with github in it)
7. after that is done run ```heroku config:set API_KEY=Your_API_Key```
8. Your_API_Key stands for the key you put in the env file in step 2

Congratulations 🍰, you have now deployed your API online.
Next integrate this with my repo @ Candy_Machine_Whitelist_Site



If you need anything you can contact me on Crypto Outcasts discord server:
https://discord.gg/KTVYs7QAfP

