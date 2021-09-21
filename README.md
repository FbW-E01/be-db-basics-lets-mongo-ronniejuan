# Backend - Database - Basics - Let's MonGO

## Let's monGO

Add your answers directly into this README file.

1. Explain ObjectIDs in MongoDB; what are they?

"ObjectIds are small, likely unique, fast to generate, and ordered." Interestingly, ObjectIds are 12 bytes long, made up of several 2-4 byte chains. Each chain represents and designates a specific aspect of the document's identity. The following values make up the full 12 byte combination (quoted from MongoDB's documentation):

"a 4-byte value representing the seconds since the Unix epoch,

a 3-byte machine identifier,

a 2-byte process id, and

a 3-byte counter, starting with a random value."
sh}


2. You have a collection called "users" with a document like this: `{ _id: 1, name: "Veera" }`. What query would you use to update the name to "Princess Veera Silkenfur"?

'db.users.updateOne( {name:"Veera"},{$set:{"name":"Princess Veera Silkenfur"}});'

3. How do you make a collection?

'db.insertOne()'
'db.createCollection("Example")


4. So the (old) mongo shell is kind of like a JavaScript REPL. What is a REPL? Which other REPL have we used?

Read Evaluated print loop; we have used node.

5. So the (old) mongo shell is kind of like a JavaScript REPL. You can use things like variables, try...catch  statements and loops. Experiment with it and find at least three other JavaScript things that we have used that work in the (old) shell. If you can, try to find even more!


6. (Research) So the old shell is pretty cool. How is the new shell better?
7. (Research) How can you insert multiple documents at the same time?


db.users.insertMany(
{ name: "Veera" },
 { name: "Rauli" }, 
 { name: "BenBen"})



8. (Research) You have a collection called `cats` with a documents like this: `{ name: "Veera" }, { name: "Rauli" }, { name: "BenBen" }` - How can you insert the field `cute: true` into all of them with one command?


db.cats.updateMany({}, {$set: { cute: true } })



9. (Task) Start a timer for 30 minutes. Spend all that time getting to know and reading https://docs.mongodb.com/manual/introduction/ - how far did you get? What was the most cool or interesting thing you learned?



10. Find one SQL Cheatsheet and one MongoDB Cheatsheet and add links to them here.


https://www.pdfprof.com/PDF_Image.php?idt=31686&t=27


































🌿
