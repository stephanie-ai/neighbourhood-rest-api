# Neighbourhood Collaboration Site

## A system to keep track of people, houses, and addresses of those houses.

</br>
1. Consider the type of data we will be storing and therefore the type of database we should implement (SQL vs NoSQL)

- We have chosen a relational database as we can organise our database by common characteristics, such as, person details and house details. This takes advantage of separation of concerns as we don't need all of the information at once.
- We will implement a SQL database. It will follow a structure handle large numbers of transactions in a single query.
</br>
2. Create a schema for this database

![alt text](schema.png)

</br>
3. Consider the requests our API should be capable of handling

- Store people, houses and addresses
- Look up a house, it’s address and owner
- Look up people in our neighbourhood within certain age brackets and with specific household sizes
</br>
4. List the routes you will need with their HTTP verb and path

    | HTTP Verb  |   Path           |
    | ---------- | ---------------- |
    | GET        | /people          |
    | GET        | /people/id       |
    | PATCH      | /people/:id      |
    | GET        | /houses          |
    | GET        | /houses/:id      |
    | GET        | /houses/:id/edit |
    | PATCH      | /houses/:id      |
    | DELETE     | /houses          |
    | GET        | /housesz         |
    | GET        | /people?minAge=30&minResidents=26        |


</br>
5. Determine the responses that should be returned and the content types of these requests and responses

        | Responses     | Content-Type |
        | ------------- | ------------ |
        | 200           | JSON  |
        | 200           | JSON  |
        | 202           | JSON  |
        | 200           | JSON  |
        | 200           | JSON  |
        | 304           | JSON  |
        | 202           | JSON  |
        | 205           | JSON  |
        | 404           | JSON  |
        | 500           | JSON  |




