# Division

Scenario: Division by 0 when operand 1 is any number

Given The calculator is on

When I type in "first number" 
And I press "divide" 
And I type in "zero" 
And I press "equals"

Then I see "Not Define" as a result

Scenario: Divide 0 by any number

Given The calculator is on

When I type in "Zero" 
And I press "divide" 
And I type in "number" 
And I press "equals"

Then I see "Zero" as a result

Scenario: Sign rules for operands

Given The calculator is on

When I type in "first number" 
And I press "divide" 
And I type in "second number" 
And I press "equals"

Then I see "the divided number with optional negative sign" as a result

Scenario: Division isn't symmetric

Given The calculator is on

When I type in "first number" 
And I press "divide" 
And I type in "second number" 
And I press "equals"

Then I see "different results when numbers are interchanged"

Scenario: Division when both operands are 0

Given The calculator is on

When I type in "Zero" 
And I press "divide" 
And I type in "Zero" 
And I press "equals"

Then I see "Not Define" as a result

Scenario: Recurring decimal case

Given The calculator is on

When I type in "first number" 
And I press "divide" 
And I type in "second number" 
And I press "equals"

Then I see "divided number and two digits of precision" as a result

Scenario: Multiple times "/" is pressed

Given The calculator is on

When I press "divide" more than one time

Then I see "one divide one time" as a result

Scenario: Interleaving of multiple operators

Given The calculator is on

When I press "plus" 
And I press "multiply" 
And I press "divide"

Then I see "divide" as a result

Scenario: When operand 2 is not present

Given The calculator is on

When I type in "first number" 
And I press "divide" 
And I press "equals"

Then I see "first number" as a result

Scenario: Division by any/all operands being fractions

Given The calculator is on

When I type in "first number" 
And I press "divide" 
And I type in "second number" 
And I press "equals"

Then I see "divided number and two digits of precision" as a result

Scenario: Division of multiple numbers

Given The calculator is on

When I type in "first number" 
And I press "divide" 
And I type in "second number" 
And I press "divide" 
And I type in "third number" 
And I press "equals"

Then I see "divided number" as a result
