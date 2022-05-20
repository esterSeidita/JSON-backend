# edgemony-course-backend

Fake REST API backend for the academic projects related to the Edgemony course.

### 1. Requirements

A [NodeJS](https://nodejs.org/en/) version from 12 to current most recent active should be fine.

### 2. Install & how to use

- Clone this repo and `cd` on the folder
- Install dependencies with `npm install`.
- Start the mock server with `npm start` and open the browser to `localhost:3004/movies` to get see the data

### 3. Fake Auth

This repo includes the `json-server-auth` package, whicj allows to simulate the authentication flows.

- users can ben created and managed in the `users` key of the `db.json` file
- login request can be done as `POST`s at the `/login` endpoint using `{ "email": "...", "password": "..." }` as body
- existing routes can be "protected" by prepending a permission code, for instance `/440/todos` rejects any request without a valid JWT token included

more details can be found in the [module documentation](https://github.com/jeremyben/json-server-auth).

### Auth Flow Frontend <--> Backend

![_img/auth-flow.png](_img/auth-flow.png)

### 3. License

MIT License

Copyright (c) 2022 Edgemony

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
