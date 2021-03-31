# LastDB
[![](https://i.imgur.com/e5laURE.png)

## About
**CAUTION
This is a really early development and please use carefully**

This is a really simple database python package using json. It's super lightweight and easy to use. 



## Install
LastDB is a pypi package so installing it is super simple!

`pip install LastDB`

## Code Example
.. code-block:: python

    import LastDB
    
    # Init the db. It will be stored in data/name_of_database.json
    db = TinyDB('name_of_database')
    
    # Specify the table
    table = db.table('users')
    
    # Insert a dict into the table
    table.insert({
        'username': 'Mikael',
        'points': 0})
        
    # Update the value of a key
    table.update(('points', 2), ('username', 'Mikael'))
    
    # Increment the value of a key by amount(default=1)
    table.increment('points', ('username', 'Mikael'), 5)
    
    # Get the value from a key 
    value = table.get('points', ('username', 'Mikael'))
    
    # Search the entire table of a match
    results = table.search(('username', 'Mikael'))
    
    # Same as search but returns a count
    count = table.count(('username', 'Mikael'))
    

## Credits
* Heavily inspired from [TinyDB](https://github.com/msiemens/tinydb).
