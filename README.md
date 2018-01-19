## Database 
CREATE TABLE books (
    book_id INT NOT NULL AUTO_INCREMENT, 
    title VARCHAR(255) NOT NULL, 
    author VARCHAR(255) NOT NULL, 
    sinopsis TEXT NOT NULL, 
    cover VARCHAR(255) NOT NULL DEFAULT 'default_cover.png', 
    PRIMARY KEY (`book_id`)
) ENGINE = InnoDB;

CREATE TABLE api_users (
    email VARCHAR(255) NOT NULL, 
    api_key VARCHAR(255) NOT NULL, 
    hit INT NOT NULL, 
    PRIMARY KEY (`email`), 
    UNIQUE (`api_key`)
) ENGINE = InnoDB;

# Slim Framework 3 Skeleton Application

Use this skeleton application to quickly setup and start working on a new Slim Framework 3 application. This application uses the latest Slim 3 with the PHP-View template renderer. It also uses the Monolog logger.

This skeleton application was built for Composer. This makes setting up a new Slim Framework application quick and easy.

## Install the Application

Run this command from the directory in which you want to install your new Slim Framework application.

    php composer.phar create-project slim/slim-skeleton [my-app-name]

Replace `[my-app-name]` with the desired directory name for your new application. You'll want to:

* Point your virtual host document root to your new application's `public/` directory.
* Ensure `logs/` is web writeable.

To run the application in development, you can also run this command. 

	php composer.phar start

Run this command to run the test suite

	php composer.phar test

That's it! Now go build something cool.
