# MOVEL CARE API CHALLENGE

## 🧪 Technologies

This project was developed using the following technologies:
- [Laravel V8] (https://laravel.com/docs/8.x/installation)
- [Passport] (https://laravel.com/docs/8.x/passport)
- [php](https://www.php.net/) >= 7.4
- [composer](https://getcomposer.org/)

## 🚀 Getting started

1. Clone the project and access the folder.

```bash
$ git clone https://github.com/m3lvin-s3rafim/movel_care_api
$ cd movel_care_api
```

2. Create an .env file in the project's root folder and copy the content from the .env.example file
3. Install project dependencies
4. Create the key in the application & Migrate the database
```bash
    php artisan key:generate
```

```bash
    php artisan migrate
```

#### 5. For testing, create the passport client and save data

```bash
    php artisan passport:client
```
# Start the project

```
$ php artisan serve
```
The app will be available for access t http://localhost:8000

## Login With Credentials
**You send:**  Your  login credentials.
**You get:** An `API-Token` with wich you can make further actions.

**Request:**
```json
POST api/auth/login
Accept: application/json
Content-Type: application/json

{
    "email": "serafimkennedy@gmail.com",
    "password": "12345678" 
}
```

## Login With OAuth2
```
POST /oauth/authorize
GRANT TYPE: authorization_code
AUTHORIZATION URL: /oauth/authorize
ACCESS TOKEN URL: /oauth/token
CLIENT ID: YOUR_CLIENT_ID
CLIENT_SECRET: YOUR_CLIENT_SECRET
```

## Personal Info

**Request:**
```json
GET api/auth/profile
Accept: application/json
Content-Type: application/json
headers: {
    'Authorization': 'BEARER ' + YOUR_ACCESS_TOKEN
  }
 
```
