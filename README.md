# email_framework

## prerequisite

Please see the  HTML structure documentation

[EMAIL FRAMEWORK](http://rappfrance.github.io/email_framework/ "Title")

(this documentation is made with gitHub pages, to update it please use the gh_page checkout)

## Technical Structure

Email framework generation made with YEOMAN & HTML EMAIL :

### YEOMAN
[yeoman.io](http://yeoman.io "Title")

Yeoman helps you to kickstart new projects, prescribing best practices and tools to help you stay productive.
To do so, we provide a generator ecosystem. A generator is basically a plugin that can be run with the `yo` command to scaffold complete projects or useful parts.

### HTML EMAIL GENERATOR
[HTMLEMAIL](https://github.com/jahvi/generator-htmlemail "Title")

A Yeoman generator to create HTML emails with built-in support for SCSS, image optimization, CSS inlining, test email delivery and more.

## Installation

1/ Clone the github repo.
2/ Configure the test email in the gruntfile.js
```
        /**
         * Test Mailer Tasks
         * ===============================
         */
        nodemailer: {
            options: {
                transport: {
                    type: 'SMTP',
                    options: {
                        service: 'Gmail',
                        auth: {
                            user: 'email@email.com', // change this with your google account
                            pass: 'passforemails' // change this with your google password
                        }
                    }
                },
                recipients: [
                    {
                        name: 'testeur',
                        email: 'test@test.com' // change this with the recipient email
                    }
                ]
            },
            dist: {
                src: ['<%= paths.dist %>/<%= paths.email %>']
            }
        }

    });
```
3/ run command
```
npm install
```
4/ to kickstart the server
```
grunt dev
```
5/ to build the project
```
grunt build
```

