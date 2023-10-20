
# Snip - A url shortener application

SNIP is a backend server for a URL shortener application. It's built using Express.js and Node.js, with MongoDB as the NoSQL database. Users can submit a title and URL to create short links. Hosted on Railway.

[Snip frontend Repo ↗](https://github.com/aakashvani/snip.com)

## Tech Stack

**Client:** Next.js, TailwindCSS

**Server:** Node.js, Express.js

**Database:** MongoDB

**Highlight:** Used SSR, CSR, NextAuth (Google)


## API Reference

#### Create a url

```http
  POST /url
```

| Body | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `title` | `string` | **Required**. A title related to url |
| `url` | `string` | **Required**. Url  |


#### Created short url

```http
  GET /url/:shortId
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `shortId` | `string` | **Required**. short id created after Post |


#### Get analytics (how many vist on shorten url)

```http
  GET /url/analytics/:shortId
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `shortId` | `string` | **Required**. short id created after Post |


#### Get all url created by a user

```http
  GET /url/all-urls/:id
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `:id` | `string` | **Required**. Id of logged in user |




## Run Locally

Clone the project

```bash
  git clone https://github.com/aakashvani/snip-server.git
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```

