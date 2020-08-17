# Addition

Scenario: Addition of two positive numbers

Given The calculator is turned on

When I type in "positive number"
And I press "plus"
And I type in "positive number"
And I press "equals"

Then I see the "added number" as the result

Scenario: Addition of two negative numbers
Given Two negative numbers
when  The calculator is turned on
And I type in "negative number"
And I press "plus"
And I type in "negative number"
And I press "equals"

Then I see the "added number" as the result

Scenario: Addition of fractions
Given Two fractions
when  The calculator is turned on
And I type in "fraction"
And I press "plus"
And I type in "fraction"
And I press "equals" 

Then I see the "added number" as the result

Scenario: Addition of +ve and -ve number
Given Two numbers one +ve and other -ve
when  The calculator is turned on
And I type in "negative number"
And I press "plus"
And I type in "positive number"
And I press "equals" 

Then I see the "added number" as the result

Scenario: Addition of decimals
Given Two numbers in decimal format
when  The calculator is turned on
And I type in "decimal number"
And I press "plus"
And I type in "decimal number"
And I press "equals" 

Then I see the "added number" as the result

Scenario: Typing operator more than once
Given one number and more than one operator
when  The calculator is turned on 
And I type in "number"
And I press "plus"
And I type in "positive number"
And I press "equals" 

Then I see the "added number" as the result

Scenario: Addition of more than 2 numbers
Given more than two numbers
when  The calculator is turned on 
And I type in "number"
And I press "plus"
And I type in "another number"
And I press "plus"
And I type in "more numbers"
And I press "equals" 

Then I see the "addition of all the numbers" as the result

Scenario: Adding numbers where the result goes out of range
Given two numbers and a suffix table
when The calculator is turned on
And I type in "number 1"
And I press "plus"
And I type in "number 2"
And I press "equals"

Then I see the "four digit output followed by a letter"


Scenario: 6+* is provided as input?
Given a number and two operators
when The calculator is turned on
And I type in "number"
And I press "plus"
And I type in "*"
And I press "equals"

Then I see the "invalid input" as a result

Scenario: Identity operation
Given two numbers 
when The calculator is turned on
And I type in "number"
And I press "plus"
And I type in "zero"
And I press "equals"

Then I see the "number" as a result

Scenario: Converse operation
Given two numbers 
when The calculator is turned on
And I type in "number"
And I press "plus"
And I type in "negative of the number"
And I press "equals"

Then I see the "Zero" as a result

