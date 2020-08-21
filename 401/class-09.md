# API Server

In Express parameters in routes can be read like:
```js
app.get('/places/:city', (req,res) => {
  // req.params.city is now a readable value
})
```

Express will let you run middleware only when certain parameters are present.

```js
router.param('city', function (req, res, next, id) {
  console.log('Only runs on routes that have a city param')
  next()
})


// That middleware will not run here
router.get('/places/seattle', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})

// That middleware does run here
router.get('/places/:city', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})

// But not here
router.get('/flights/to/:airport', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})
```

Mongoose is a structured ORM that gives structure to our Mongo documents. By default NoSQL Databases have no structure. This way is easier to model a collection to add the user collections. keeping the data the same by creating a schema helps with the modeling of the collections.

By sharing the schema as a sud-doc doesn't connect the data and needs to be managed to bring in actual data.
```js
var childSchema = new Schema({ name: 'string' });
var house = new Schema({ address: 'string', city: 'string', state: 'string' });

var adult = new Schema({
  // Array of subdocuments
  children: [childSchema],

  // Single nested subdocuments.
  address: house
});
```

You can link two collections together such as players collection and a sports team collection. 
`populate()` can be used to connect 2 collections.

Virtual Joins create a virtual field by connecting with named fields. Then using populate me find/laod docs. 
```js
const teams = mongoose.Schema({
  name: { type:String, required:true },
}, { toObject:{virtuals:true}, toJSON:{virtuals:true} });

teams.virtual('players', {
  ref: 'players',
  localField: 'name',
  foreignField: 'team',
  justOne:false,
});

teams.pre('find', function() {
  this.populate('players');
});
```










