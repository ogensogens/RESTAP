const express = require('express')
const bodyParser = require('body-parser');
const nodeTutorialApp = express();
const port = 3500

// Middleware
nodeTutorialApp.use(bodyParser.json());

//Routes
nodeTutorialApp.get('/user', (req, res) => {
    const user = {
        name: 'gerald',
        age: '30',
        sex: 'Male'
    }
    res.json(user);
})

// Server
nodeTutorialApp.listen(port, ()=> {
    console.log(`This server is running on port ${port}`)
})
