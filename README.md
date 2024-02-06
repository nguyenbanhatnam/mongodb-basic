1. **Basic CRUD Operations:**
- Create a new database called "mydatabase".
    ```javascript
    use mydatabase
    ```
- Create a collection called "users".
   ```javascript
   db.createCollection("users")
   ```
- Insert a few documents (user data) into the "users" collection.
   ```javascript
   db.users.insertMany([
    {name:"Nam", age:23}, 
    {name:"Dat", age:23}, 
    {name:"Duy", age:23}, 
    {name:"Tam", age:23}])
    ```
- Retrieve all documents from the "users" collection.
   ```javascript
   db.users.find()
   ```
- Update a document in the "users" collection.
   ```javascript
   db.users.updateOne({name:"Nam"},{$set:{IsHandsome:true}})
   ```
- Delete a document from the "users" collection.
   ```javascript
   db.users.deleteOne({name:"Tam"})
   ```

2. **Querying:**
- Find all users who are older than 30.
   ```javascript
   db.users.find({age:{$gt:30}})
   ```
- Find all users who have a specific email address.
   ```javascript
   db.users.find({email:{$exists:true}})
   ```
- Find all users whose name starts with a specific letter.
   > db.users.find()
- Find all users sorted by their age in descending order.
   > db.users.find().sort({age:-1})
- Find the oldest user.
   > db.users.find().sort({age:-1}).limit(1)

3. **Indexing:**
   - Create an index on the "age" field.
   - Create a compound index on the "name" and "email" fields.

4. **Aggregation:**
   - Calculate the average age of all users.
   - Group users by their age and count how many users are in each age group.
   - Find the user with the highest age.
   - Find the user with the lowest age.
   - Calculate the total age of all users.

5. **Data Modeling:**
   - Design a schema for a blog application including collections for users, posts, and comments. Define relationships between these collections.
   - Implement the schema in MongoDB, including necessary indexes.

6. **Advanced Queries:**
   - Find users who have commented on a specific post.
   - Find posts created by users who are older than 25.
   - Find all comments made on posts created in the last month.
   - Find users who have not posted anything yet.

7. **Data Import/Export:**
   - Import user data from a JSON file into your MongoDB database.
   - Export the "users" collection to a JSON file.

8. **Replication and Sharding:**
   - Set up replication for your MongoDB instance.
   - Configure sharding for your database.

These exercises cover a range of MongoDB functionalities and will help you gain proficiency with MongoDB. Feel free to modify or expand upon them based on your learning goals and interests.