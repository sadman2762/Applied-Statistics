# Applied-Statistics(Homework Solution)

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
    (given sum - 1)/18 [general formulae]
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
### 13.Two soldiers shoot on a target in turn until the first hit. The probability that the starter hits it is 0.4, while the second hits it with probability 0.35. What is the probability that the first successful shot belongs to the soldier who started the shooting?
    (0.4)*(1/(1-(0.6)*(0.65))

### 14.The ten digits are written on ten separate cards. A card is chosen randomly, the digit on is noted and the card is replaced. How many cards should be chosen to have at least one number greater than 7 among them with probability greater than 0.75?
    
     log(1-0.75)/log(1-0.2)
 ### 15.Create a MATLAB function that approximates the probability in the following experiment with simulations!


Two dice are rolled. Find the probability that they show different values, given at least one of them shows six.

The number of simulation should be N = 10^3. The variable p should store the approximation, i.e. the relative frequency.

Use semicolons when defining variables!

With the Check button the code is free to run.





For example:

Test	Result
rand('seed',20);
disp(sim());
0.900929
Answer:(penalty regime: 0 %)

    function p = sim()
    N  = 10^3;
    d1=randi(6,2,N);
    f6=sum(d1(1,:)==6 | d1(2,:)==6);
    fd6=sum((d1(1,:)==6 | d1(2,:)==6) & (d1(1,:) ~= d1(2,:)));
    p =  fd6/f6   ;
    end
### 16.Create a MATLAB function that approximates the probability in the following experiment with simulations!

Three dice are rolled. Find the probability that the sum of the numbers obtained is 8 given the sum is even.

The number of simulation should be N = 10^3. The variable p should store the approximation, i.e. the relative frequency.

Use semicolons when defining variables!

With the Check button the code is free to run.





For example:

Test	Result
rand('seed',301);
disp(sim());
0.2
Answer:(penalty regime: 0 %)

    function p = sim()
    N  = 10^3;
    d1=randi(6,3,N);
    d1=sum(d1);
    d2=sum(d1 == 8);
    d3=sum(mod(d1,2)==0);
    p =d2/d3     ;
    end


### 17.Three dice are rolled till the first six appears on one of them. What is the mean number of rolls required, inclusive the last one?

        1/(1-(5/6)^3)
        1/(1-(5/6)^n) where n is number of dice

### 18.The cost of a lottery coupon (5 from 90) is 300 HUF. In case of two winning numbers hit the lottery pays 1400 HUF, a triple pays 19500 HUF, four winning numbers result 1.05 million HUF while a fiver pays 1500 million HUF. Buying a single coupon what is the average gain?

        (1400*nchoosek(5,2)*nchoosek(85,3))/nchoosek(90,5) + (19500*nchoosek(5,3)*nchoosek(85,2))/nchoosek(90,5) + (1.05*10^6*nchoosek(5,4)*nchoosek(85,1))/nchoosek(90,5) +                 (1500*10^6*nchoosek(5,5)*nchoosek(85,0))/nchoosek(90,5) - 300

### 19.The nominal value of a share is 4 golden galleon. In a year the value either can doubled, or halved or remain the same - each of the events has the same probability. The same happens in the following years, independently of the events of the previous year. Find the distribution of the value of the share after 3 years. What is the mean and the variance of the value?​

Hint:
If X,Y independent, then E(XY)=EX⋅EY


Eξ=
        
        4*(3.5)^3/27

D2ξ=
        
        4*4*(2*2 + 1*1 + 0.5*0.5)^3/27 - (4*(3.5)^3/27)^2


### 20.Create a MATLAB function that approximates the expected value in the following experiment with simulations!

Three dice are rolled till the first one appears on one of them. What is the mean number of rolls required, inclusive the last one?​

The number of simulation should be N = 10^3. The variable m should store the approximation, i.e. the mean.

Use semicolons when defining variables!

With the Check button the code is free to run.

Answer:(penalty regime: 0 %)

        function m = sim()
    N  = 10^3;
    s = 0;
    for i = 1:N
        while true
            s = s+1;
                if rand()<1/6 || rand()<1/6 || rand()<1/6
                    break;
                end
            end
        end
    

    m = s/N    ;
    end
### 21.A stick of length 12 meters is randomly broken into two parts. Find the cumulative distribution function (CDF) and the probability density function (PDF) of the length of the shorter part.

### Cumulative Distribution Function (CDF)
#### Cumulative distribution function: F(x):
      0 if x<0;
      x/6 if x<6;
      1 if x>6;
#### Probability density function.: f(x)
    1/6 if 0<x<6;
    0 otherwise
### 22.Find the CDF of the distance of two randomly chosen points of the [0,2] interval.
#### Cumulative distribution function: F(x):
      0 if x<0;
      1-(1-x/2)^2 if 0<x<2;
      1 if x>2;
### 23.The PDF of a random variable ξ is
#### Probability density function.: f(x)
    0 if x < 3;
    A/(5+x)^2 if x>= 3
#### What is the value of A?    
    5+3 = 8
#### What is the value of P(3<ξ<13)?
    1 - (5+3)/(5+13)
#### Cumulative distribution function: F(x):
    0 if x < 3;
    1 - 8/(5+x) if x>=3;
