# 1 inventory:
```
db.inventory.insertMany(
    [
        {_id:1,item:{name:'ab',code:'123'},qty:10, tags:['A','B','C']},
        {_id:2,item:{name:'cd',code:'123'},qty:11, tags:['D','E','M']},
        {_id:3,item:{name:'ef',code:'456'},qty:12, tags:['F','B','D']},
        {_id:4,item:{name:'gh',code:'456'},qty:13, tags:['G','O','C']},
        {_id:5,item:{name:'ij',code:'567'},qty:10, tags:['A','E','D']},
        {_id:6,item:{name:'ij',code:'567'},qty:10, tags:[['A','B'],'D']},
        {_id:7,item:{name:'ij',code:'567'},qty:10, tags:['A','B']}
    ]
    );
```

# 2. inventory
```
db.inventory.drop();
db.inventory.insertMany(
    [
        {_id:1,item:{name:'ab',code:'123'},qty:10, tags:['A','B','C']},
        {_id:2,item:{name:'cd',code:'123'},qty:11, tags:['D','E','M']},
        {_id:3,item:{name:'ef',code:'456'},qty:12, tags:['F','B','D']},
        {_id:4,item:{name:'gh',code:'456'},qty:13, tags:['G','O','C']},
        {_id:5,item:{name:'ij',code:'567'},qty:10, tags:['A','E','D']},
        {_id:6,item:{name:'ij',code:'567'},qty:10, tags:[['A','B'],'D']},
        {_id:7,item:{name:'ij',code:'567'},qty:10, tags:['A','B']},
        {_id:8, item:{name:'ab'}},
        {_id:9, qty:15},
        {_id:10,item:{name:'ab'}, qty:'20'}
    ]
    );
  
```

# 3. budget
```
db.budgets.drop();
db.budgets.insertMany([
    {_id:1, category:'food', budget:500, spent:450},
    {_id:2, category:'clothes', budget:1000, spent:750},
    {_id:3, category:'drink', budget:200, spent:550},
    {_id:4, category:'travel', budget:350, spent:550},
    {_id:5, category:'medicine', budget:500, spent:600},
    {_id:6, category:'misc', budget:400, spent:400},
]);
```
