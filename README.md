# Alright Wordpress

Basic Wordpress install, configured with Dotenv and deployed to Fortrabbit

## Requirements
- MAMP
- PHP 5+
- MySQL 5+

## Local Development

*Local development requires MAMP.*

1. Install Composer dependencies
```
$ composer install
```
2. Start MAMP and create a new host and a database on `localhost`.
3. Copy `.env.example` to `.env` and set proper database configuration.
4. Done! Navigate to your new site in your browser and run the Wordpress installation.

## Deploying to Production

1. Add Fortrabbit as a GIT remote, named `production`.
2. Run the `deploy.sh` script. Your GIT password is the fortrabbit account password.

```
$ sh scripts/deploy.sh
```

This will do a few things - compress assets, commit those as a new deployment to the repo, and push to the `production` branch.