java cName: ________________

Section: _______________

Statistics Assignment #1
Descriptive Statistics (5 points)
Marketing Research


INSTRUCTIONS:
This assignment must be completed individually. This means that you may not ask any person other than the professor for help. You are permitted to use the internet to look up how to perform certain operations in JASP or to look up certain statistical concepts. You can use generative AI (e.g., ChatGPT) to ask questions about what a certain term may mean or look up how to perform a certain operation in JASP. You may not use AI to generate answers for any of these questions. If you have any question, please ask the professor directly.
Instructions for this assignment assume that you are using JASP. You may use a different statistical software (e.g., SPSS, Stata, R) if you like, but it is your responsibility to make sure that the results, graphs, etc. from this software match the correct JASP output. Additionally, copy/pasting outputs directly from JASP into Word may cause some issues (e.g., table columns may not be properly aligned). As a result, I recommend that you screenshot the JASP output and then copy the screenshot into Word rather than just using the copy/paste function in JASP. You may not use Excel for this assignment.
For early assignments, I will give you relatively detailed instructions about how to perform certain functions and tests in JASP and notes to go with them. Please note that these instructions apply to the most recent version of JASP (version 0.19.3) for macOS. Older versions of JASP or JASP running on Windows or Linux may differ slightly. Once we have covered a certain function, the instructions will be less detailed. You should go back and look at old assignments and questions to see the more detailed notes on a certain function. 
Finally, a few questions from this assignment will appear in some form on the final exam. These questions are marked with (EXAM). This means that the concept covered by this question will be tested on the exam. It does not mean that the exact question itself will be on the exam. 


For this assignment, please use the “IMDb Data.csv” file posted on Canvas.
This data file has the following variables:
Rank: IMDb rank in the for the last 10 years
Title: Name of the movie
Genre: Genre of the movie
Description: Brief description of the plot
Director: Director of the movie
Actors: List of actors in the movie
Year: Year that the movie was released
Runtime: Length of the movie (in minutes)
Rating: Average viewer score (on a 1 to 10 scale)
Votes: Number of viewer ratings
Revenue: Millions of dollars made at the box office
Metascore: The average critic score (converted to a 1 to 100 scale)



Question 1 (1.25 points total):

Load your data. 

Click the menu button (three horizontal blue lines) on the top right
Click on “Open”  “Computer”  “Browse”
Navigate to the file you want to load (in this case “IMDb Data.csv”) and click “Open”
The data should appear in the main window of JASP

Create a table showing the average (mean) Metascore per movie, grouped by genre. 
Click the “Descriptives” icon at the top of the window (it should be near the left side)
This should open up a new menu on the side of the screen that has a list of the variables in the data on the top left
Move the variable you are interested in describing (in this case “Metascore”) to the section that says “Variables.” You can drag and drop it there or click on “Metascore” and then click the right arrow next to the variable list
Move the variable you are interested in grouping by (in this case “Genre”) to the section that says “Split.” Again, you can drag and drop it or click on “Genre” and then click on the right arrow next to the “Split” section
Depending on how your window is set up, you may see a table automatically appear on the right side of your screen. If you do not see it, click the arrow all the way on the right side of your screen. This should make the table visible (and will likely hide the original dataset from view). You can change what shows up on your screen by playing with the bars that divide the different sections of the screen (you can drag them to change the size of the different sections or click the arrows to hide/show different sections).

a.Copy/paste your output below.  Hint: There are 13 genres, so the table should have 13 columns. (0.25 points)


b.On average, which genre had the lowest Metascore? (0.25 points) 


c.What was the average Metascore of movies in this genre? (0.25 points) 

d.Which genre has the highest standard deviation for Metascore? (0.25 point)

e.Which genre has the largest range of Metascore (i.e., which genre has the largest difference between the highest and lowest Metascore)? (0.25 points)
Question 2 (0.75 points total):
Create a crosstab showing the number (count) of movies released in each genre for each year. (Hint: There are 11 years and 13 genres, so your output should have 1代 写program、c/c++，Java
代做程序编程语言1 columns and 13 rows. There will also be a couple of extra rows for the row/column labels and for the row/column totals). 
Click on “Frequencies” icon at the top and choose “Classical”  “Contingency Tables.” 
Contingency Tables (also known as crosstabs) show the number of observations across different groups within the data. 
Choose the two variables you want to count by and assign one to “Rows” and one to “Columns.” It doesn’t matter which you put in which spot. It will give you the same information, just flipped.
You may notice that JASP does not allow you to put the “Year” variable in the “Rows” or “Columns” section. This is because “Year” is coded as a continuous variable (also known as a “scale” variable in JASP) in the dataset. In most cases, it is impossible to make a contingency table using a continuous variable since you would need to have different columns for 2010.125, 2010.126, 2010.127, etc. 
However, “Year” is actually not continuous. It is an ordered categorical variable (there is no year 2011.2, it just jumps from 2011 to 2012). So we need to change how JASP thinks about the “Year” variable. 
To do that, we need to go back to the dataset (click on the “Edit Data” button at the top). Click on the “Year” variable. Go to the top where it says “Column Type” (it should be at the top left), and change the column type from “Scale” to “Ordinal.” Now go back to creating the contingency table (click on the “Analyses” button at the top) and try again. 

a.Copy/paste your output below. (0.25 points)



b.Which year had the most movies listed in the top 1000? (0.25 points) 



c.In what year were the fewest Adventure movies in the top 1,000 released? (0.25 points)  



Question 3 (1 point total):
Imagine that you want to know how much professional critics and regular IMDb reviewers agree on their ratings of movies. To do this, create a variable that calculates the difference between “Rating” and “Metascore.” Call this new variable “Difference.” 
(Hint: Because the Metascore is on a 100 point scale and Rating is on a 10 point scale, you should multiply the Rating by 10 to put them both on a 100 point scale.) 
Go back to the “Data” view. 
Click the black plus sign (+) near the top row of the data. A window should pop up that says “Create Computed Column.” Give the new column a name. In this case, call it “Difference.” Below the variable name, you should see two rows of icons. One has an R and one has a hand. I think the “R” option is easier. Click that one. Then there are four options for the type of variable you are creating. In this case, you are creating a “scale” variable. Click that and then click “Create Column.”
When the popup closes, you will go back to your data. Go to your new column and double click on the variable name. It will open a new menu at the top of the page.
Under “Computed column definition” type the formula for your new variable. In this case, it is “(10*Rating) – Metascore” Then click “Compute column.” The column should now be filled with the correct calculated values.

Now create a table that shows the mean (average) difference by genre. Hint: Use the same type of table that you used in Question 1 (but with new variables). 
a.Copy/paste your output below. (0.5 points)



b.On average, which genres did regular IMDb reviewers like less than professional critics? That is, for which genres was the Rating less than the Metascore?  (0.5 points)



Question 4 (2 points total) (EXAM)
Imagine that you are a new marketing executive at a movie studio. You are being asked to figure out a way to help your studio better compete in a changing media landscape where fewer people are seeing movies in theaters.

1.Provide two possible “goals” that you might have at the beginning of this project. Remember, your goal should be a “maximization” or “minimization” goal. For example, one goal may be to “Maximize the number of people who see our movies in the theater.” Refer to the Week 2 slides for examples. (0.5 points total, 0.25 points each)

Goal 1:

Goal 2:


2.Think about Goal 1 that you listed above. What are two constraints that might be useful to consider when researching how to achieve that goal? For example, two constraints for the goal “Maximize the number of people who see our movies in the theater” could be “People can’t see more than one movie in a day” or “There are only 5,000 movie theaters in the United States.” Refer to the Week 2 slides for examples. (0.5 points total, 0.25 points each)

Constraint 1:

Constraint 2:

3.What are (at least) two variables in the dataset we used in this assignment (i.e., in “IMDb Data.csv”) that could provide useful information to help you achieve Goal 1? Hint: A description of the variables in the dataset can be seen at the beginning of this assignment. (0.5 points total, 0.25 points each)


4.How would you use these variables to develop a strategy that could achieve Goal 1? (0.5 points)

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
