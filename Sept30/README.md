**Sept 30 Assignment Updates **

I wanted to try to do the data visualization project because I wanted to see if I cold challenge myself. 

As someone who struggles a lot with mental health, I wanted to use a dataset regarding mental health in Nepal because it is avery negleced area of research and resources. Unsurprisingly, there were no datasets available. I looked online and found a dataset on depressive episodes in the US. 

When I tried first importing the file, I simply copy pasted the names from the folders it was kept in to my code. 

```
 strings = loadStrings("Users/macbookair/Desktop/samhsa-major-depressive-episode/data/2012_2014_substate_sae_table_27.csv");
```
I knew there were no mistakes in the names but processing kept saying the it couldn't load the file. I couldnt figure out why. I renamed the file to a single word and shifted it to the desktop and it loaded then. I don't understand why it didn't work with the longer name given that it was the same code.  


After this, I wanted to simply try and create circles in random positions on the canvas, with its size fluctuating depending on the rate of depressive episodes. I used the following code: 
```
void draw () {
  String data[];
  int row=0;
  data = split(strings[row], ","); 
  float circSize;
  circSize = row[4];
  circle (random(500), random(500), circSize); 
  row = row + 1;
  
}
```
I thought this would work quite well because I was creating an array that stored the values from the csv file then use the value of the array for the circSize. I got the error "The type of the expression must be an array type but it resolved to int" I googled what this meant but the examples were very complex and did not help me in any way. I experimented with a few things and the error went away but when it came to displaying the circle, nothing showed up. I started getting confused by my own code and realized I don't think my code worked because it didn't neccesarily seperate the string into the seperate row that I needed it to. I tried thinking of differnt ways to increase or change the variable or arrays to make sure that when the data is split it split the rows, but I couldn't visualize it. Hence, I decided to restart, and this time use the Table function. 
