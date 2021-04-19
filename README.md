This is a small project developped while learning MongoDB, Express, React-Redux, NodeJS development.
It was also deployed online using Heroku for the backend and Netlify for the front-end.
Live demo can be accessed at https://tender-bassi-a35c3b.netlify.app/

**Features**
- API for CRUD purpose, using Axios
- Like function (working as a counter)
- Edit button populates form thanks to drilling
- Form changes depending if it's creating or editing a post
- Image upload using Base64
- Dispatching and Reducers using Redux
- Front-end design using @material-ui/core & /icons
- Component styling using @material-ui/core/styles

Requires node.js to run as well as Mongodb Atlas

**MongoDB connection**

create **CONNECTION_URL** into **.env file**, equal to MongoDB connection string

```
CONNECTION_URL = mongodb+srv://userid:password@cluster0.f9zrm.mongodb.net/myFirstDatabase?retryWrites=true&w=majority
```

OR

in **/server/index.js** file

**add**

```
const URL = "mongodb+srv://userid:password@cluster0.f9zrm.mongodb.net/myFirstDatabase?retryWrites=true&w=majority"
```

**edit** connection function to use **URL** instead of **process.env.CONNECTION_URL**

```
mongoose.connect(URL, { useNewUrlParser: true, useUnifiedTopology: true })
    .then(() => app.listen(PORT, () => console.log(`Server running on port ${PORT}`)))
    .catch((error) => console.log(error));
```
    
 **Start servers**
 
1. Open terminal
2. cd into /server/
3. Run `npm start`
4. Open second terminal
5. cd into /client/
6. Run `npm start`
