Requires node.js to run as well as Mongodb Atlas


**MongoDB connection**

create CONNECTION_URL into .env file, equal to MongoDB connection string

```
CONNECTION_URL = mongodb+srv://userid:password@cluster0.f9zrm.mongodb.net/myFirstDatabase?retryWrites=true&w=majority
```

OR

in index.js file

add 

```
const URL = "mongodb+srv://userid:password@cluster0.f9zrm.mongodb.net/myFirstDatabase?retryWrites=true&w=majority"
```

edit connection function to use URL instead of process.env.CONNECTION_URL

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
