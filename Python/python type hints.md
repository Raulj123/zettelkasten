Python has support for optional "type hints" (also called "type annotations").
These **"type hints"** or annotations are a special syntax that allow declaring the type of a variable.
By declaring types for your variables, editors and tools can give you better support.
* Main place to declare type hints is function parameters 
* #### Simple types
	* ```int```, ``` float ```, ``` bool ```, ``` bytes ```
* #### Generic types
	* internal values for ```dict```, ```list```,```set```,```tuple```
* ### Who cares?
	* you get -> completion, error checks

``` python
def sayhello(first_name: str, last_name: str)
def data(myset: set [str, str, int], mydic: dict[str, int])
def maybeNone(id: int | None)     # only in python 3.10+

import typing from Union          # python 3.8+
def maybeNone(id: Union[int, None])

# Clases as types
class Person:
    def __init__(self, name: str):
        self.name = name


def get_person_name(one_person: Person):
    return one_person.name
```

# Pydantic models
* declare the shape of data as classes with attributes
* each attribute has a type
* create an instance with values it will validate -> convert them to right type if that is the case and give me object with all data
``` python 
from datetime import datetime

from pydantic import BaseModel


class User(BaseModel):
    id: int
    name: str = "John Doe"
    signup_ts: datetime | None = None
    friends: list[int] = []


external_data = {
    "id": "123",
    "signup_ts": "2017-06-01 12:22",
    "friends": [1, "2", b"3"],
}

# the ** takes the key value pairs and unpacks them as key=word arguments
user = User(**external_data)
print(user)
# > User id=123 name='John Doe' signup_ts=datetime.datetime(2017, 6, 1, 12, 22) friends=[1, 2, 3]
print(user.id)
# > 123
```
