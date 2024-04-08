# 4.3 Logical Operators

Up until this point, we have only worked with boolean expressions with **one** comparison in it. There are another set of operators: **`logical operators`**. We can use logical operators in combination with comparison operators to create more complex boolean expressions.

There are three logical operators:
1) `and`
2) `or`
3) `not`

## The `and` Operator
Consider the example: ABC University’s Computer Science program requires a **Grade 12 math credit** `and` **an overall average of 80% or higher**. Below is a table of students applying for the program and their credentials coming out of high school:

| Student | Courses                                                                                  | Overall Average |
| ------- | ---------------------------------------------------------------------------------------- | --------------- |
| Doug    | Visual Arts, Law, Vocal, Theatre, History, Phys. Ed                                      | 72%             |
| Stu     | Physics, French, Phys. Ed, Biology, History, Math (Calculus)                             | 77%             |     
| Alan    | Visual Arts, Law, Vocal, Theatre, History, French                                        | 91%             |
| Phil    | Chemistry, Math (Adv. Functions), Phys. Ed, Visual Arts, Biology, Math (Data Management) | 85%             |

When deciding which students get accepted to the computer science program, ABC University must check whether each student meets their conditions.  The following table summarizes their findings:

| Student | Has Grade 12 Math Credit? | Average >= 80%? | Has Gr.12 Math Credit **`and`** Average >= 80% |
| ------- | ------------------------- | --------------- | -------------------------------------------- |
| Doug    | _____                     | _____           | _____                                        |
| Stu     | ____                      | _____           | _____                                        |
| Alan    | _____                     | ____            | _____                                        |
| Phil    | ____                      | ____            | ____                                         |

The table above illustrates the properties of **`and`**. If a and b are conditions that evaluate to True or False, the result the expression a and b can be summarized in the following Truth Table:

### The `and` Truth Table
| a | b | a **`and`** b |
| - | - | ------------- |
| F | F | F             |
| F | T | F             |
| T | F | F             |
| T | T | T             | 

 <span style="color:red">
<b>NOTE: Both</b> a and b must be True for a AND b to evaluate to True
</span> 

## The `or` Operator
Consider the example: The sequel to The Social Network, “The Social Network: Eduardo Strikes Back” is coming out this Friday.  The movie is rated 18A, meaning adults or those accompanied by an adult can see the movie. The following people want to see the movie

| Name(s) | Age | Accompanied by Adult |
| ------- | --- | -------------------- |
| Gabi    | 13  | No                   |
| Michael | 19  | No                   |
| Elliot  | 16  | Yes, with mother     |
| Mary    | 25  | Yes, with friend     |

When deciding who gets to see the movie, the box office cashier must check to see if the admission conditions for this movie have been met.  The following table summarizes their findings:

| Name(s) | Age >= 18? | Accompanied by Adult? | Able to Watch Movie? |
| ------- | ---------- | --------------------- | -------------------- |
| Gabi    | _____      | _____                 | _____                |
| Michael | ____       | _____                 | ____                 |
| Elliot  | _____      | ____                  | ____                 |
| Mary    | ____       | ____                  | ____                 |

### The `or` Truth Table
| a | b | a **`or`** b |
| - | - | ------------ |
| F | F | F            |
| F | T | T            |
| T | F | T            |
| T | T | T            | 

<span style="color:red">
<b>NOTE: As long as at least one of a or b is True, it will evaulate to True.</b>
</span> 

## The `not` Operator
Quite simply, the not operator allows us to reverse the result of a boolean expression.  Consider the boolean expression `1 < 2`, this would evaluate to `True`.  The expression `not(1 < 2)` would result to `False`.

### The `not` Truth Table
| a | not(a) |
| - | ------ |
| F | T      |
| T | F      |

## Examples
### Example #1:
```python
age = 16
withAdult = True

print (((age >= 18) or (withAdult)) == (not(age >=18) and not(withAdult)))
```
> **<ins>OUTPUT:</ins>**<br>
> 

### Example #2:
```python
age = 16
withAdult = True

print (((age >= 18) or (withAdult)) == ( not(age >=18 and withAdult)))
```
> **<ins>OUTPUT:</ins>**<br>
> 