# 123
app.post("/notes",(request,response) -> {

MongoClient.connect(CONNECTTON_URL, { useNewUr1Parser: true }, (error, client) -> {
     if(error) {
        response.send(error);
        throw error;
}
database -client.db(DATABASE_NAME);
collection - database.collection("Notes");

collection.insert (request.body,(error,result) => {
    if(error) {
        return response.status(500).send(error);
    }
    response.send(result.result);
   }):
});
});
}):


app.get("/notes", (request, response) => {
MongoClient.connect(CONNECTTON_URL, { useNewUr1Parser: true }, (error, client) -> {
     if(error) {
        response.send(error);
        throw error;
}
database -client.db(DATABASE_NAME);
collection - database.collection("Notes");

collection.insert (request.body,(error,result) => {
    if(error) {
        return response.status(500).send(error);
    }
    response.send(result.result);
   }):
});
});
}):

app.put('/notes/:id', (resquest,response) => {
     if(error) {
        response.send(error);
        throw error;
}
database -client.db(DATABASE_NAME);
collection - database.collection("Notes");

collection.find({})/toArray((error, result) -> {
if(error) {
response.send(result[numberID]._id);
return response.status(500).send(error);
}

var numberID - parseInt(request.params.id):


if (numberID >-result.length)
    response.send("Not enough elements in database")
else
{
  
  collection.update({"_id":result[numberID]._id},{$set:{"body":request.body.body}})
  response.send("Updated!");
 }
});
});
});

app.delete('/notes/:id', (resquest,response) => {
     if(error) {
        response.send(error);
        throw error;
}
database -client.db(DATABASE_NAME);
collection - database.collection("Notes");

collection.find({})/toArray((error, result) -> {
if(error) {
response.send(result[numberID]._id);
return response.status(500).send(error);
}

var numberID - parseInt(request.params.id):


if (numberID >-result.length)
    response.send("Not enough elements in database")
else
{
  
  collection.remove({"_id":result[numberID]._id},(err, result) => {
  if(err){
  response.send("result[numberID]);
  throw err;
  }
  response.send('user deleted');
 });
 }
});
});
});

    
