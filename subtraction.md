# Subtraction

Scenario: subtraction of two positive numbers and first is greater than the second

Given The calculator is on

When I type in "positive number"
And I press "minus"
And I type in "positive number"
And I press "equals"

Then I see the "subtracted number" as the result

Scenario: Subtraction of two negative numbers and first is less than the second

Given The calculator is on

when I type in "first number"
And I press "minus"
And I type in "second number"
And I press "equals"

Then I see the "subtracted number and a minus sign as prefix" as the result

Scenario: Subtraction of one positive number and negative number

Given The calculator is on

when I type in "positive number"
And I press "minus"
And I type in "negative number"
And I press "equals"

Then I see the "subtracted number" as the result

Scenario: Subtraction of two fractions

Given The calculator is on

when I type in "fraction"
And I press "minus"
And I type in "fraction"
And I press "equals"

Then I see the "subtracted fraction" as the result

Scenario: Subtraction of two decimals

Given The calculator is on

when I type in "decimal"
And I press "minus"
And I type in "decimal"
And I press "equals"

Then I see the "subtracted decimal" as the result

Scenario: Typing operator more than once

Given The calculator is on

when I type in "first operator"
And I press "minus"
And I type in "second operator"
And I press "equals"

Then I see the "first operator replaces the second operator" as the result

Scenario: Subtraction of two more than two numbers

Given The calculator is on

when I type in "first number"
And I press "minus"
And I type in "second number"
And I press "minus"
And I type in "third number"
And I press "equals"

Then I see the "subtracted number with minus sign as prefix" as the result

Scenario: Subtraction of two numbers and the result goes out of range

Given The calculator is on and a suffix table

when I type in "first number"
And I press "minus"
And I type in "second number"
And I press "equals"

Then I see the "four digit number followed by letter" as the result

Scenario: 6-* is input

Given The calculator is on

when I type in "number"
And I press "minus"
And I type in "*"
And I press "equals"

Then I see the "invalid input" as the result

Scenario: Identity Operation

Given The calculator is on

when I type in "number"
And I press "minus"
And I type in "Zero"
And I press "equals"

Then I see the "subtracted number" as the result

Scenario: Converse Operation

Given The calculator is on

when I type in "zero"
And I press "minus"
And I type in "negative of a number"
And I press "equals"

Then I see the "negative of number" as the result
