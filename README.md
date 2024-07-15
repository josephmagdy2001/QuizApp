
### About QuizApp

A fully functional quiz application developed on TALL stack and filamentphp3.


### Setup

## Clone the master repo
```
git clone <repo>
cd <repo>
alias sail=./vendor/bin/sail

```


## Execute initial setup and seeding.
```
cp .env.example .env

composer install

sail up -d

sail npm install

sail npm run build

sail artisan migrate:fresh

sail artisan make:filament-user

sail artisan db:seed

sail artisan shield:super-admin

sail artisan db:seed --class ShieldSeeder


sail npm run dev #should be kept open if using local dev env
```


# Loing to admin:

http://localhost/admin/


# Login to user:
http://localhost/member/


* Edit the admin user and set is_admin to yes on edit form and save -- this will enable switching between user and admin roles for admin from profile menu:

![Screenshot from 2024-02-24 20-17-47](https://github.com/aliaxonbaig/quizapp/assets/52659978/3279ca12-a1c7-443a-9372-c7849cc8e516)



![Screenshot from 2024-02-24 20-18-36](https://github.com/aliaxonbaig/quizapp/assets/52659978/6a5115de-61ef-4fb3-bcd2-fc4dfdd68251)

#Create a test user from admin and assign user role
#Login as test user and i) Subscribe to the certification under subscription menu and then the subscribed quiz certificaitons will appear in the quiz drop down for selection.



## Screenshots
Admin Dashboard

![Screenshot from 2024-02-24 19-02-12](https://github.com/aliaxonbaig/quizapp/assets/52659978/476ccdcb-488d-4356-ad3b-b4adb3e80252)

Sections Administration:
![Screenshot from 2024-02-24 19-03-07](https://github.com/aliaxonbaig/quizapp/assets/52659978/37fcdc7e-19d5-4912-a91b-ac990d0b79f4)


User Dashboard:
![Screenshot from 2024-02-24 19-07-25](https://github.com/aliaxonbaig/quizapp/assets/52659978/b30abd3d-fe8f-4062-929f-77f3b3cefcb5)



Subscription Page: #This could be bootstraped with some subscription for enabling payment and premium services for members with some additional improvements:
![Screenshot from 2024-02-24 20-21-31](https://github.com/aliaxonbaig/quizapp/assets/52659978/a8cacb15-9f6f-484d-a578-b383cf6f49f3)

Quiz Selection:


Quiz In-Progress:
![Screenshot from 2024-02-24 19-05-31](https://github.com/aliaxonbaig/quizapp/assets/52659978/c8f67330-e28b-478e-9a23-b341e1425210)


Quiz Result Review:
![Screenshot from 2024-02-24 19-07-01](https://github.com/aliaxonbaig/quizapp/assets/52659978/489d6bc0-39db-4245-8480-1bcc7dd52929)

Quiz Overview Page:
![Screenshot from 2024-02-24 19-07-37](https://github.com/aliaxonbaig/quizapp/assets/52659978/47aabf4e-6808-43eb-83d9-f0c60966ae0a)




## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The app is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
