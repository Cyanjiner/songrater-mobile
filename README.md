# Songrater-app

### Deployed Website: [https://songrater-comp333.firebaseapp.com/](Link to Songrater)
### Heroku Django Backend: [https://songrater-comp333.herokuapp.com/api/](https://songrater-comp333.herokuapp.com/api/rating/)

## Instructions

### 1. Setting up
#### 1.1 Creat the Virtual Environment
- Install the virtual environment, `django-react`, with:
```shell
python3 -m venv django-react
```

- Activate your virtual environment with (leave out `.fish` if you are using the default shell):
```shell
source django-react/bin/activate.fish
```
#### 1.2 Django dependencies
- Install dependencies with:
```shell
python3 -m pip install django
python3 -m pip install djangorestframework
python3 -m pip install django-cors-headers
python3 -m pip install django-filter
python3 -m pip install django-rest-knox
```

- Lastly, run server for backend with:
```shell
cd backend
python3 manage.py runserver
```

#### 1.3. React dependencies
- Open another terminal (let's call it terminal 2), and cd to songrater-app directory with `cd songrater-app`.

- React requires node.js and its package manager npm. If you have not done so,
  install NPM with `npm install`.

  In case of a `React Native Expo - Node.js version xxx is no longer supported`
  error message, you can run `sudo npm install -g n` and `sudo n latest`. `-g`
  stands for global, i.e., every users on your computer.

- We will be using the Expo CLI development environment.
  If you have not done so, install the expo command line tools with `npm install -g expo-cli`.

- In order to have the iOS simulator and tools available install Xcode via the App.

- Install dependencies with:
```shell
npm i @react-native-asyncstorage
npm install @react-navigation/native @react-navigation/stack
npm install react-hook-form
npm install react-native-reanimated@~2.2.0
expo install expo-font
expo install expo-app-loading
```

### 2. Run the App
2.1 Backend
```shell
cd hw03-main/backend
python3 manage.py runserver
```
2.2 Frontend
```shell
cd hw03-main/frontend
npm install
```
```shell
npm start
```
OR
```
expo start
```

- In the opening browser window (Connection: LAN) click run on iOS simulator. If there is an error, try running `expo upgrade`.

- The Expo server can be stopped with `ctrl + c`.
###3. How to Use the Songrater App

#### Register or Login
If you have already created an account you can login in, otherwise click on the "Register Button". After you have registered, you should be redirected to the login page where you can login.

#### create new song
If you want to add a new song, click "new song" and add information.

#### update song information
click the song tile and press the edit button. this will bring you to a page to edit the song title and artist

#### add/update your rating
click the song tile and click on the number of stars you want to rate the song. click rate. this will either update or add your rating.

#### delete song
To delete a song, click on the songtile and then press the delete button

###4. Test APIs using Postman for user authentication
---------------------------------------------------------------------------------------------

If you want JUST WANT to test the backend, please check the following.

### Test APIs using Postman for user authentication
Download desktop client from Postman at <https://www.postman.com/downloads/>.

#### Registration:
To send a POST request to <http://127.0.0.1:8000/api/auth/register> via Postman, you can choose Content-Type as `key` and application/json as `value` in the `Headers`. Then in the `body`, select `raw` and include the following:
```shell
{
    "username": "jinerzheng",
    "password": "12345"
}
```
And then click on `send`. If successfully registered, you should be able to see a token generated.

#### Login:
To send a POST request to <http://127.0.0.1:8000/api/auth/login> via Postman, just do the same steps as above (put in the same username and password after you registered successfully). After you get a token, copy that for user authorization.

#### User Authorization:
Now, send a GET request to <http://127.0.0.1:8000/api/auth/user>, you need to choose Authorization as `key` and paste the token you get from log-in with 'Token ' in front of it as `Value` in the `Headers`. For example: "Token 78d2b3c0edc368eb416c0a76e55a6378df3ddb1721137ca5571d1cd69c3bcc06"

## Contributions
Tanya, Tomoshi, Jiner
