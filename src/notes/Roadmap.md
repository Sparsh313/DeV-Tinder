# Basic Steps For making a Website

1>Install [express];

2>[app.listen(7797)];

3>DB (atlas , compass , install Mongoose)

4>[mongoose.connect] (URL) {AsyncAwait}

5>phele [DB_connect] kro phir listen kroo (export ConnectDB to app.js and vha .then krke connect kro )

6>Create [Schema]

7>GET POST PATCH DELETE (/api) to DB from POSTMAN
[CRUD]
\*\*\*
[req.body] jo hai wo undefined show hogaa hameshaa kyuki Node JSON file read ni kr pata uske liye ham ek middleware use krege to change
the format of JSON into JS object using Express_in_Built_Middleware :
[app.use(express.json())]

8>Validation , Data sanitization (mostly used in Post Patch Api)

9>Encryption

10>JWT

> instal jsonwebtoken(jwt)
> create a token =>> jwt.sign({ id: user.id },Secret_key)
> Send/assign token to user=>> res.cookie("token",token)
> cookie-parser npm library =>> app.use(cookieParser())
> Now while calling an api we will request cookie from user and extract token from that
> now verify the token => jwt.verify(token,Secret_key) =>This will return id of user (hidden msg whie jwt.sign())
> now put all this in auth middleware

11>Create route handlers //auth req

12>Connection schema
//request- validations/rateLimiter/customize msgs

13>Indexing-To prevent server to hang (Fast response)

- Unique-true (index auto true)

14>UserAuth

15>Populate using refrence

16>feed Api (most important)
// maan lo maine kisi ko req bheja ya kisi ne mujhe req bheja to meri feed me koi show ni hogaa
// eg. Sparsh -> alia , ridhima -> sparsh
// sparsh ko to na alia show hogi na ridhima

17>Pagination

> /feed?page=1&limit=10 //First 10 users query=> .skip(0) & .limit(10)
> /feed?page=2&limit=10 //11-20 users query=> .skip(10) & .limit(10)
> /feed?page=3&limit=10 //21-30 users query=> .skip(20) & .limit(10)
