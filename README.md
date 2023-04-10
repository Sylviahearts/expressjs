# expressjs


const express = require('express');
const bodyParser = require('body-parser');

const app = express();
const port = 5000;

app.get('/', (req,res) => {
 return res.send("Hello");
});

app.use(bodyParser.urlencoded({extended: false}));

app.get("/user",function(req, res){
    const user ={
        name: "sylvia" ,
        age: "20",
        sex: "female",
    };
    res.json(user);
});

app.listen(port,() => console.log(`server listening on port: ${port}`))
