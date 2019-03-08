1. Restaurante concept: 
starting from the simplest
mono menu per day, starting from 500 meals, no more than 2000.
price: 10 dollar per meal
gross margin: >50%, EBITDA >20%
payment: at day 0, 100 meals for free, paid by the restaurant. customer pay whatever amount for tomorrow customer. 
subsequent days, day(i) customer paying for day(i+1), only sell to the amount that was paid by the previous day; if day(i). total >1000, the extra will be part of the social fund
calculation: assume all goes well (day.total >=10000), open 20 days a month, per month income 100K
salary for cook, cleaner, payment (by cash or QR code transfer)

2. TripAdvisor ranking based on recent ratings/taking out best 1% and worst 1%, looking at rating patterns...
3. Main() mystery in running unittest. 
There are many ways to run the unittest in PyCharm, 
1). in Terminal, $ python3 unittest
2). ctrl + R, run the test file .py 
3). click on the "run test" green arrows beside the line numbers, on the left hand side of your code.
4). wrap up a unittest.main() under ```if __name__ == '__main__':```, then run it

Possible explanations. 
1). ```class TestProgram``` is not really documented 
2). without the main(), unittest can ran normally. I suspect once we do ctrl + R, the program actaully do run the tests. However there is a main() in the end, the program then go to main() again to run the program
Testing the theory.
By debugging the code, I step into the first line in test_file after importing unittest and the file that needed to be tested. That first line defines the ```class Testfile(unittest.TestCase)```. In the "Variables" tab, I see that __name__ is immediately defined as ```__name__ ={str}'test_file'```. Stepping down, the methods are being executed one by one. Until it reaches my second breakpoint: the ```if __name__== '__main__':``` statement. Because the __name__ is not __main__, then of course the unittest.main() is not executed and just skipped. 

3). unittest.main() on the same level as the test methods.

4). unittest.main() on the same level as the test class.
