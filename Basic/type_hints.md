# Type Hints

## Understanding the problem

פייתון היא שפה שסוגי המשתנים מוחלטים בה באופן דינמי בזמן ריצה, זה עלול להוביל לתקלות רבות.
אולי בקוד קצר ופשוט זה לא מרגיש כמו בעיה רצינית אבל בפרוייקטים גדולים זה לעלול ליצור בעיות שקשורות לסוג משתנה שמוגדר בזמן אמת.

## The solution - Type Hints

זה פיצר שנוסף ב2015 בגרסת פייתון 3.5
זה מאפשר לנו להחליט מה הסוג המצופה של משתנה

### Advantages

**הקוד שלנו הופך ליותר מובן**

**תופס שגיאות מוקדם יותר - לא יהיה מקום לשגיאות שעלולות להגיע בהפתעה**

**תמיכה של העורך קוד שלנו** העורך קוד יבין איזה משתנה אנחנו משתמשים ויתן לנו השלמות אוטומטיות מתאימות


## Basic Usage

*שימוש פשוט :*

```bash
number : int = 10
```
באמצעות נקודיים אנחנו מפרטים את סוג המשתנה
פה יצרנו משתנה אינטגר עם ערך של 10

*אנחנו לא חייבים לתת ערך :*

```python
number : int
```

בזמן הריצה פשוט לא יהיה ערך למשתנה 

*שימושים פשוטים  נוספים :*

```python
def foo(number : int) -> int:
    return number
# this function gets an Integer and returns an Integer
```


```python
def foo(number : int) -> int:
    return number
# this function gets an Integer and returns an Integer
```


```python
def foo(var : int | str):
    pass
# this function gets an Integer or a String
```


```python
def foo(var : int | None = None):
    pass
# this function gets an Integer or None

foo(10)
foo()
foo(None)

foo("Banana") # this is raise an error
```

## שימוש יותר מתקדם

חשוב לציין מדובר בסטנדרט - כול פרויקט שנעשה נצטרך לוודא שהמשתנים בו מוגדרים.
ככול שנעמיק בפייתון נלמד יותר ויותר סוגים של משתנים כול דבר חדש שנלמד - שגם אותם נצטרך ללמוד להגדיר

כול מה שעברנו עליו בעמוד הזה היה דברים מאוד בסיסיים
תמשיכו לחקור ותראו שאתם מבינים להגדיר את כול סוגי המשתנים ומבני הנתונים שאתם מכירים והגדרה של סוגים (Type Alias)

שימו לב שיש הבדלים בין הגרסאות של פייתון , אז יכול להיות שתראו דברים סותרים בזמן המחקר שלכם - הם לא סותרים הגרסאות פשוט שונות

## חומרים

סביר להניח שבמחקר שלהם תתקלו בדברים שלא למדתם עדיין , תבינו מה שרלוונטי אליכם .

>[סרטון הסבר](https://www.youtube.com/watch?v=BzBUagNkX1E)

> [סרטון הסבר נוסף](https://www.youtube.com/watch?v=QORvB-_mbZ0)

> [דוקומנטציה רשמית - typing](https://docs.python.org/3/library/typing.html)





