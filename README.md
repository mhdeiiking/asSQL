# Document For AsSQL

<b>Download it using pip:</b>
* `` pip install asSQL ``
<pre></pre>
<b>On Pypi:</b>
* <a href="https://pypi.org/project/asSQL">asSQL</a>

<pre></pre>
# To setup personal account and an Database Table in db:
``
import asSQL
from asSQL import Client 
app = Client("username")
db = app['table_name']
db.create_table()
``
# To add an data to db :
``
data_here = 1 # Please note: this function allow (List,Bool,Dicts,String,Integer,etc..)
db.set("key_name",data_here)
``
# To get key data:
``
key = db.get("key_name")
print(key)
``
# To delete a key and the data:
``
db.delete("key_name")
``
# To get all keys from database table:
``
a = f"{db.keys()}".split() # get it in a list []
print(a)
``
# To get all keys and data at same time in a design:
``
print( db.get_all() )
``
# To check if key are exists:
``
key_name = "d"
print(db.key_exists(key_name))
# Note if return ( 0 ) That means None exists, and if ( 1 ) Thats mean are True or exists.
``
# To push a elemnt to list '[]':
``
lista = []
db.set("list",lista)
element = "new"
db.push("lista",element) # must be list [].
``
# To unpush a elemnt from list '[]':
``
lista = []
db.set("list",lista)
element = "new"
db.unpush("lista",element) # must be list [].
``
# To get all user's table:
``
print(db.tables())
``
