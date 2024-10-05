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


      
