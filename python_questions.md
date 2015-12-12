# PageDNA python exercises

1. Implement `flatten_list` such that `ListTestCase` passes

~~~
import unittest

def flatten_list(l):
    pass

class ListTestCase(unittest.TestCase):
    def test_flatten_list(self):
        l = [[[1, 2, 3], [4, 5]], 6]
        self.assertEqual(flatten_list(l), [1,2,3,4,5,6])
        l = [None, [], [[1, 2, [[]], [3]], [[4], 5]], 6]
        self.assertEqual(flatten_list(l), [None,1,2,3,4,5,6])
~~~

2. What would be a better name for the following function?

~~~
def function(n):
    if n < 2:
        return n
    else:
        return function(n-1) + function(n-2)
~~~

3. Write a better implementation of function(n).

4. What is the value of function(113)?

5. Given the following:

~~~
| src         | dst         |
|-------------+-------------|
| nyc         | chicago     |
| chicago     | kansas city |
| chicago     | phoenix     |
| kansas city | nyc         |
| nyc         | kansas city |
~~~

   Represent the data statically, and implement a function `all_trips(src, dst)`
   that returns all possible trips between `src` and `dst`. For example,

   all_trips('nyc', 'kansas city')

   should return

   [['nyc', 'kansas city'], ['nyc', 'chicago', 'kansas city']]
