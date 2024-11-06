# Next.js CMS Blog with MongoDB

A serverless web application that utilizes Next.js and MongoDB to create a custom-built content management system for managing and publishing blog content.

![test](https://github.com/Samuellaudev/samuellaudev/blob/9837c53d8b21118b0ecd2335926f0249a585e004/public/images/projects/NextJs_v14_Blog_CMS_with_MongoDB.png?raw=true)

## 🔗 URL

[Next.js CMS Blog](https://nextjs-mongodb-cms.vercel.app/)

## 🚀 Features

- Show all posts in home page and blog page
- Add, edit or delete post in edit-mode (Admin only)
- Utilized Vercel's Serverless Functions to interact directly with MongoDB
- Upload image using Cloudinary
- User management system using JWT authorization with HttpOnly Cookie
- Implementing Stripe payment gateway (Test Mode) for premium content access
- Dark Mode integration

More project details [here](https://www.samuellau.dev/projects/nextjs-blog-with-mongodb)

## 🛠 Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start
```

## Required Environment Variables

The `.env` file contains environment variables that are accessible to code in the Next.js app via the process.env object.

Multiple dotenv files can be created to configure different environments. `.env` is the base file that applies to all environments, you can also create `.env.development` for dev specific variables, `.env.production` for prod and `.env.local` for the local environment.

### Adresse public du blog :

Le titre du site/blog

```
FRONTEND_NAME="My RP Blog"
```

exemple d'adresses :

```
FRONTEND_URL=http://localhost:3000
FRONTEND_URL=https://rp-blog.vercel.app
FRONTEND_URL=https://rpg.kalak.xyz
```

### Access MongoDB Database

The `MONGO_URI` environment variable is used to store the connection string for the MongoDB database. This connection string includes information such as the database protocol, username, password, host, port, and database name.

Here's an example of how you might define the MONGO_URI in your `.env` file:

```
MONGO_URI=mongodb+srv://username:password@cluster0.mongodb.net/mydatabase?retryWrites=true&w=majority
```

### Access resend.com API

For contact form:

Resend is an email API for developers. It allows you to send transactional emails with a simple API call. You can use Resend to send emails from your applications, automate email workflows, and more.

https://resend.com/docs/api-reference/api-keys/create-api-key

```
RESEND_API_KEY
```

For user signin/forgot password:

```
SMTP_HOST
SMTP_EMAIL
SMTP_PASSWORD
```

In both cases, you must define name from sender:

```
SENDER_NAME="My RP Blog"
```

### JWT Secret to keep your connection secure

The `JWT_SECRET` environment variable is used to sign and verify JWT tokens for authentication, change it with your own random string to ensure nobody else can generate a JWT with the same secret to gain unauthorized access to your Next.js app or API. A quick and easy way is join a couple of GUIDs together to make a long random string (e.g. from https://www.guidgenerator.com/).

For detailed explanation on how things work, check out [Next.js docs](https://nextjs.org/docs).
