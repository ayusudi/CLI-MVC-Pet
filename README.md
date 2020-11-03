# MVC ANIMAL 

**INFO :**
```
 index.js -----> controller  -------
                                   |
                                   v
  view  <--- controller  <----  model
```

class Animal 
- nama 
- type  
- height 
- weight 
- age
- healthStatus

```
Commands : 
$ node index.js help
$ node index.js read
$ node index.js create <name> <type> <height> <weight> <age> <healthStatus>
$ node index.js delete <id>
$ node index.js isHealthy <id>
$ node index.js isUnhealthy <id>
```

## RELEASE 0 

> $ node index.js help  

Output : 
```
    Commands : 
    $ node index.js help
    $ node index.js read
    $ node index.js create <name> <type> <height> <weight> <age> <healthStatus>
    $ node index.js delete <id>
    $ node index.js isHealthy <id>
    $ node index.js isUnhealthy <id>
```
untuk `node index.js` juga menampilkan hal yang sama 

## REALEASE 1 
> $ node index.js read
```
ID.  Name,   Infomation
1. Luffy, HeathStatus : false
```

Jika data lebih dari 2 maka
```
ID.  Name,   Infomation
1. Luffy, HeathStatus : false
2. Hewan2, HeathStatus : status2
3. Hewan3, HeathStatus : status3
4. Hewan3, HeathStatus : status3
etc..
```

## RELEASE 2 
> $ node index.js create <name> <type> <height> <weight> <age> <healthStatus>

Example :  
node index.js create PomPom Turtle 3 0 3 false

Output  
(Contoh disini total dijson 2)
```
Berhasil menambahkan hewan dengan nama "PomPom". Sekarang total data adalah 2. 
```

## RELEASE 3
> $ node index.js delete <id>

Success Example:   
node index.js delete 1  
```
BERHASIL MENGHAPUS DATA
Data saat sejumlah [total data]
```

Failed Example:  
node index.js delete 9999   
Untuk id yang tidak ditemukan, outputnya : 

```
DATA WITH ID 100 IS NOT FOUND
```


### RELEASE 4

> $ node index.js isHealthy <id>

Example : 
node index.js isHealthy 2 
```
2. Pompom, healthStatus ✅
3. Pemy, healthStatus ✅
4. Luffy, healthStatus ❌
```

> $ node index.js isHealthy <id>


Example : 
node index.js isUnhealthy 2 
```
2. Pompom, healthStatus ❌
3. Pemy, healthStatus ✅
4. Luffy, healthStatus ❌
```