# Internals And Descriptors

## חומרים

[about Globals](https://www.geeksforgeeks.org/python/python-globals-function/)

[about Locals](https://www.geeksforgeeks.org/python/python-locals-function/)

## עוד דברים שקורים מאחורי הקלעים

מה קורה כאשר אנחנו יוצרים אובייקט ? 
(רוב האובייקטים עובדים ככה , בהמשך ניגע למה)
אז ככה . כאשר אנחנו יוצרים אובייקט מוצמד לאובייקט הזה מילון נסתר - __dict__ . זה קורה באופן אוטומטי.
וכול המידע של האובייקט הזה נשמר שם

```python
class Dog:
    def __init__(self, name : str):
        self.name = name

my_dog = Dog("Rex")


print(my_dog.__dict__) 
# output should be: {'name': 'Rex'}
```

## אז לא בדיוק

רשמנו שזה קורה ברוב המקרים , אז צריך להסביר מתי זה לא קורה ככה.
מילון זה מבנה יקר במבחינת זיכרון אז פייתון עובד קצת אחרת בחלק מהמקרים : 

**built in types** - אובייקטים בסיסיים ממומשים ב - C בצורה יעילה . ללא מילון פנימי . 

**__slots__** - אופציה שניתן להשתמש בה , מחליף את המילון במבנה אחר שנקרא סלוט. מבנה זול יותר. 

במחלקות שאנחנו יוצרים יהיה לנו מילון פנימי אלא אם נגדיר סלוט


## Descriptors

[about Descriptors](https://www.geeksforgeeks.org/python/descriptor-in-python/)

