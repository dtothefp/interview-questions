# Interviewing Web Developers

This repository is a compilation of useful interview questions for web developers.

Click through the link at the bottom of each problem to see the solution. All solutions are implemented in JavaScript.

## General Questions

#### 1. Internet Protocols

If I type https://google.com into my browser and press enter, what happens?

[See a sample answer](http://stackoverflow.com/a/2092602/2117153)

#### 2. Front-end Performace

How would you go about optimizing the front-end performance of a JavaScript web application?

[See a sample answer](solutions/general/frontend-perf.md)

#### 3. Cross-Domain Issues

What is the difference between CORS and JSONP? Under what circummstances would you use each?

[See the answer](http://stackoverflow.com/a/12309651/2117153)


## JavaScript

#### 1. String manipulation

Define a `spacify` function which takes a string as an argument and returns the same string, but with each character separated by a space.

[See the answer](solutions/javascript/spacify.js)

#### 2. Prototypes

Create the same `spacify` function, but add it directly as a method to the `String` object. Talk about this practice as it relates to building real applications.

[See the answer](solutions/javascript/spacify-string.js)

#### 3. Scope

What will the result of the following be?

```javascript
var User = {
    count: 1,
    getCount: function() {
        return this.count;
    }
};
console.log(User.getCount());

var func = User.getCount;
console.log(func());
```

How would you ensure that the context of func() is always bound to User such that 1 will be returned?


[See the answer](solutions/javascript/scope.js)

#### 4. More String Manipulation

Implement an algorithm to determine if a string has all unique characters.

[See the answer](solutions/javascript/string-manipulation.js)


## Algorithms

#### 1. Bubble Sort

What is the complexity of the bubble sort algorithm? Use Big-O notation.

Implement it.

[See the answer](solutions/algorithms/bubble-sort.js)


#### 2. Merge Sort

What is the complexity of the merge sort algorithm? Use Big-O notation.

Implement it.

[See the answer](solutions/algorithms/merge-sort.js)

#### 3. Quick Sort

What is the complexity of the quick sort algorithm? Use Big-O notation.

Implement it.

[See the answer](solutions/algorithms/quick-sort.js)


#### 4. Binary Search

What is the complexity of a binary search? Use Big-O notation.

Implement it.

[See the answer](solutions/algorithms/binary-search.js)

#### 5. Linked Lists

Given the following implementation of a Linked List node:

```javascript
function Node(data) {
    this.data = data;
    this.next = null;
}
```

Write code to remove duplicates from an unsorted linked list given the first node in the list.

[See the answer](solutions/algorithms/linked-list.js)

FOLLOW UP: How would you do this without access to a buffer?

#### 6. Binary Tree Inversion

Given the following implementation of a binary tree node:

```javascript
function TreeNode(val) {
    let node = {};
    node.val = val;
    node.left = node.right = null;
    return node;
}
```

Write a function that takes the root element of the tree and inverts the tree.

[See the answer](solutions/algorithms/binary-tree-inversion.js)

#### 7. Breadth First Search

Given a graph represented as an adjacency list and the node to start with, return an array of the graph's nodes in depth first order

[See the answer](solutions/algorithms/breadth-first-search.js)


## Logic / Brain Teasers

#### 1. Fizzbuzz

Write a function that prints the numbers from 1 to 100.

For multiples of three print "Fizz" instead of the number.

For multiples of five print "Buzz" instead of the number.

For multiples of both three and five print "FizzBuzz".

[See the answer](solutions/logic/fizzbuzz.js)

#### 2. Palindromes

Write a function to check if a string is a pallindrome.

[See the answer](solutions/logic/pallindrome.js)

#### 3. Array Reverse

Write a function to reverse an array.

Now do it without using any array API methods.

Now do it without a buffer.

[See the answer](solutions/logic/array-reverse.js)

#### 4. Array Flatten

Write a function that flattens a multi-dimensional array of unknown depth and composition into a one-dimensional array.

[See the answer](solutions/logic/array-flatten.js)

#### 5. Pascal's Triangle

Pascal's triangle is a triangular array of the binomial coefficients. This means that in Pascal's triangle, each number is the sum of the two directly above it. Here's an illustration:

![pascal's triangle](http://www.mathsisfun.com/images/pascals-triangle-4.gif)

Write a function that prints row N of Pascal's triangle.

[See the answer](solutions/logic/pascals-triangle.js)

#### 6. Fibonacci

The Fibonacci sequence is a series of numbers where each number in the sequence is the sum of the previous two numbers. For this question, assume that the sequence starts with the number 0. The first ten numbers of the sequence look like this:

`0, 1, 1, 2, 3, 5, 8, 13, 21, 34`

Write two functions to compute the n'th number of the Fibonacci sequence.

The first function should use an iterative method.

The second function should use a recursive method.

[See the answer](solutions/logic/fibonacci.js)


#### 7. Duplicate Characters

Write a function that removes any duplicate characters from a string.

[See the answer](solutions/logic/remove-dupes.js)


#### 8. Greatest Prime Factor

Write a function that finds the greatest prime factor of a number n.

[See the answer](solutions/logic/largest-prime-factor.js)

#### 9. Finding Sum Pairs

Write a function that finds all pairs of integers in an integer array that sum to n

[See the answer](solutions/logic/sum-pairs.js)

#### 10. Monitoring Frankenzombie

The evil Professor Boolean, after years of hard work, has finally created his first successful Frankenzombie specimen. In order to understand the creature, the professor has tasked his minions with monitoring it.

Unfortunately, Professor Boolean's minions are a bit disorganized. There may be times when more than one minion is monitoring at once! Thankfully, the minions are at least organized enough to clock their hours.

Write a function that takes a list of minion timesheets `[start, end]` and returns the total number of hours that Frankenzombie was monitored. All values `start` and `end` are greater than zero and no greater than 2^30-1. `end` will always be greater than `start`.

[See the answer](solutions/logic/frankenzombie.js)


## Systems Design

#### 1. REST API Design

Image that you are building Twitter. In particular, you are in charge of designing an API for Twitter's backend. This API will be used by a developer building a 3rd party Twitter client. What actions would you expose and what HTTP method would you use for each?

What are some ways you could scale your Twitter service to accomodate a high user load?

What are some ways you could scale your Twitter service to

[See a sample answer]()

#### 2. URL Shortening

Design a URL shortening service like bit.ly. Touch upon each of the following:
    - The service's database architecture
    - The service's API
    - The service's frontend web app

[See a sample answer]()

## Application Security


#### 1. Cross Site Scripting

What is XSS and what does the acronym stand for? How is the exploit executed and what is its potential impact? How can it be mitigated?

[See a sample answer](solutions/appsec/xss.md)

#### 2. SQL Injection

What is SQL Injection? How is the exploit executed and what is its potential impact? How can it be mitigated?

[See a sample answer](https://www.owasp.org/index.php/SQL_Injection)

#### 3. Cross-site Request Forgery

Imagine that we have an online baking app protected by a login. Once a user has logged in, they're given a session cookie that they must have in order to send HTTP requests to the rest of the app.

For simplicity's sake, assume that the main dashboard page consists of nothing but a form that allows the user to send money to other users.
The app has two fields - a dollar amount field and a username field - and a submit button.
Submitting the form hits the following endpoint of the bank's backend API at `https://www.example.com/transfer?amount=1000&destination=desiredUser`, which gets the current user, queries the database to make sure the user has enough money to send the transaction, and then updates the sender's and `desiredUser` balances in the DB.
    - What security flaw exists in this system?
    - Can you elaborate on how precisely the user would exploit this flaw to steal money from a user?
    - How could this flaw be mitigated?

[See a sample answer](solutions/appsec/csrf.md)
