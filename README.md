# Applied-Statistics

## Important questions list for Midterm
### 1.In an urn there are 18 red and 16 white balls. We choose 7 balls without replacement. What is the probability, that all chosen balls are red?
    nchoosek(18,7)/nchoosek(34,7)
### 2.In an urn there are 16 red and 16 white balls. We choose 5 balls without replacement. What is the probability, that we choose 2 red and 3 white balls?
    nchoosek(16,2)*nchoosek(16,3)/nchoosek(32,5)
### 3.8 people are having a dinner at a round table. What is the probability that two women don't sit next to each other, if there are 4 men and 4 women?
    factorial(3)*factorial(4)/factorial(7)
### 4.In an urn we have 7 red balls. Find the minimal number of white balls to be added to have the probability of choosing a white ball at least 0.45.
    x /(x+7) > 0.45
    x /(x+a) > 0.45 [general formulae]

### 5.In 24 hours, time two ships arrive independently into the harbour of Chewbakka Bay, denoted by A and B, respectively. Ship A can be unloaded in 3 hours, while ship B in 3 hours. Workers start to unload a ship immediately after it's arrival and if the other ship arrives before they finish it has to wait. What is the probability that none of the ships has to wait?
    ((24-3)^2 + (24-3)^2) /(2*(24)^2)
    ((24-a)^2 + (24-b)^2) /(2*(24)^2) [general formulae]
### 6.A stick of length one meter is randomly broken into two parts. What is the probability that from the obtained parts and from a new stick of 0.9 meter length a triangle can be formed?
    0.9
    always same probability of new stick

### 7.Two dice are rolled. Find the probability that the sum of the numbers obtained is 6 given the sum is even.
    5/18
### 8.We know that at least one of the seven kids in a family is a girl. Find the probability of having also a boy in the family.
    1-(1/2)^7
    1-(1/2)^(number of kids)
### 9.In a TV quiz show the player must choose one from four envelopes. In the first envelope there are 4 cards saying 'Sorry, next time', 8 cards with 'You have won 100 euros' and 5 cards with 'You have won 500 euros'. The content of the second envelope: 9 cards 'Sorry, next time', 6 cards 'You have won 100 euros' and 2 card 'You have won 500 euros'. The third and fourth envelope contain only 'Sorry, next time' cards. The player chooses randomly an envelope and from the chosen envelope he chooses a card. What is the probability that the player wins 500 euros?
    (5/17)*(1/4) + (2/17)*(1/4)
    total probability theorem.
### 10.Rust Rider cars are produced in four factories. The first factory produces 420 cars per day, the second 150, the third 120, while the fourth 810. The refuse ratios for the factories are 1%; 6%; 9% and 5%, respectively.
### What is the probability that we find a junk car?
    (1/100)*(420/1500) + (6/100)*(150/1500) + (9/100)*(120/1500) + (5/100)*(810/1500)
    total probability theorem.
### We bought a Rust Rider and we found it perfect. What is the probability that it had been produced in the second factory?
    ((94/100)*(150/1500))/((99/100)*(420/1500) + (94/100)*(150/1500) + (91/100)*(120/1500) + (95/100)*(810/1500))
    bayes theorem
### 11.Create a MATLAB function that approximates the probability in the following experiment with simulations!

Two fair dice are thrown. Find the probability that the sum of the numbers obtained is 8.

The number of simulation should be N = 10^3. The variable p should store the approximation, i.e. the relative frequency.

Use semicolons when defining variables!

With the Check button the code is free to run.

For example:

Test	Result
rand('seed',36);
disp(sim());
0.141
Answer:(penalty regime: 0 %)
    
    function p = sim()
    % Megoldás tömbökkel:
    N  = 10^3;
    d  = randi(6,2,N);
    s  = sum(d);
    k  = sum(s==8);
    p  = k / N;
    end
### 12.Create a MATLAB function that approximates the probability in the following experiment with simulations!


Two fair dice are thrown. Find the probability that the two numbers equal.


The number of simulation should be N = 10^3. The variable p should store the approximation, i.e. the relative frequency.

Use semicolons when defining variables!

With the Check button the code is free to run.





For example:

Test	Result
rand('seed',51);
disp(sim());
0.168
Answer:(penalty regime: 0 %)

    function p = sim()
    N  = 10^3;
    d1 = randi(6,1,N);
    d2 = randi(6,1,N);
    p  = sum(d1 == d2) / N;
    end

      
