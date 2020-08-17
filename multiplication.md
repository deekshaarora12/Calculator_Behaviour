Scenario: Result overflow

Given The calculator is on and a suffix table

When I type in "first number"
And I press "multiply"
And I type in "second number"
And I press "equals"

Then I see the "multiplied output followed by letter" as the result

Scenario: Signs of the numbers

Given The calculator is on

When I type in "first number with negative sign"
And I press "multiply"
And I type in "second number with positive number"
And I press "equals"

Then I see the "multiplied output and a minus sign as prefix" as the result

Scenario: Zero value multiplication

Given The calculator is on

When I type in "number"
And I press "multiply"
And I type in "Zero"
And I press "equals"

Then I see the "Zero" as the result

Scenario: Multiplication by 1

Given The calculator is on

When I type in "number"
And I press "multiply"
And I type in "One"
And I press "equals"

Then I see the "number" as the result

Scenario: Decimal value multiplication

Given The calculator is on

When I type in "decimal number"
And I press "multiply"
And I type in "decimal number"
And I press "equals"

Then I see the "multiplied output with two precision" as the result

Scenario: Irrational value multiplication

Given The calculator is on

When I type in "irrational number"
And I press "multiply"
And I type in "irrational number"
And I press "equals"

Then I see the "multiplied output rounded of to two digit precision" as the result

Scenario: Simple multiplication

Given The calculator is on

When I type in "number"
And I press "multiply"
And I type in "number" 
And I press "equals"

Then I see the "multiplied number" as the result

Scenario: Rational multiplication

Given The calculator is on

When I type in "rational number" 
And I press "multiply" 
And I type in "rational number" 
And I press "equals"

Then I see the "multiplied rational number" as the result

Scenario: Decimal & integer multiplication

Given The calculator is on

When I type in "decimal" 
And I press "multiply" 
And I type in "integer" 
And I press "equals"

Then I see the "multiplied output rounded of to two digit precision" as the result

Scenario: More than two numbers multiplication

Given The calculator is on

When I type in "first number" 
And I press "multiply" 
And I type in "second number" 
And I press "multiply" 
And I type in "third" 
And I press "equals"

Then I see the "multiplied number" as the result

Scenario: Complex number multiplication
Given The calculator is on

When I type in "complex number" 
And I press "multiply" 
And I type in "complex number" 
And I press "equals"

Then I see the "multiplied output as complex number" as the result

Scenario: Range of operand exceeds allowed limit

Given The calculator is on

When I type in "first number" 
And I press "multiply" 
And I type in "second number" 
And I press "equals"

Then I see the "input out of range" as the result

Scenario: Pressing "multiply button" multiple times

Given The calculator is on
 
And I press "multiply button multiple times" 

Then I see the "multiply button single occurence" as the result

Scenario: Interleaving operators (Press *, then press /, then press +)

Given The calculator is on

When I press "multiply" 
And I press "divide"  
And I press "plus"

Then I see the "plus operation" as the result

Scenario: Decimal value capping

Given The calculator is on

When I type in "ten digit decimal number" 

Then I see the "I cannot add more digits"
