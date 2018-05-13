# -devchallenge.it - qa - 1

Steps to reproduse:
1. Install and open "Postman" on your computer
2. Go to http://petstore.swagger.io/

-----------------------------------------------------POST METHOD (create new pet)---------------------------------------------

3. Open "Postman" and chooose "POST" method; URL: http://petstore.swagger.io/v2/pet
4. Click on "Body" tab -----> "raw" -------> JSON (application/json)
5. in text field add next code: 


{
  "id": 0,
  "category": {
    "id": 0,
    "name": "string"
  },
  "name": "Hello_World",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "string"
    }
  ],
  "status": "available"
}


6. Click "Send" (Steps you can see on screenshot: http://take.ms/dZ2gd
7. Check Status (expected: 200 OK)

---------------------------------------------------GET METHOD (check if pet was added)--------------------------------------------


8.For check pet added choose method "GET"; URL: http://petstore.swagger.io/v2/pet/-9223372036854775808
where:  -9223372036854775808 id of created pet
9. Ckick "Send" 
10. Check Status (expected: 200 OK)


----------------------------------------------------PUT METHOD (for change pet name)----------------------------------------------

11. Change name: choose method "PUT"; URL: http://petstore.swagger.io/v2/pet
12. In body tub use next code:
{
  "id": 0,
  "category": {
    "id": 0,
    "name": "string"
  },
  "name": "Goodbye_World",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "string"
    }
  ],
  "status": "available"
}
13. Ckick "Send" 
14. Check Status (expected: 200 OK)

--------------------------------------------GET METHOD (check if pet name was changed)-------------------------------------------


15.For check pet added choose method "GET"; URL: http://petstore.swagger.io/v2/pet/-9223372036854775808
where:  -9223372036854775808 id of created pet
16. Ckick "Send" 
17. Check Status (expected: 200 OK)
18. Check if the name was changed (expected name: Goodbye_World)

-------------------------------------------------------DELETE METHOD (delete your pet)-----------------------------------------------

19. For delete pet choose method "DELETE"; URL: http://petstore.swagger.io/v2/pet/-9223372036854775808
where:  -9223372036854775808 id of created pet
20. Ckick "Send" 
21. Check Status (expected: 200 OK)

----------------------------------------------------GET METHOD (check if pet was deleted)-----------------------------------------

22. For check if ped deleted choose method "GET"; URL: http://petstore.swagger.io/v2/pet/-9223372036854775808
where:  -9223372036854775808 id of created pet
23. Ckick "Send" 
24. Check Status (expected: 404 Not Found) http://take.ms/e7BXA
