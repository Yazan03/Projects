The source code : 


```python
import zipfile
f="gfg.zip"
obj=zipfile.ZipFile(f)

with open("rockyou.txt",'rb') as passlits:
    for i in passlits:
        for j in i.split():
            try:
                obj.extractall(pwd=j)
                print("The password is : ",j.decode())
            except:
                continue
```                
