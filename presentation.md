# Stardew Valley Farm Analyzer - 2 Minute Talk

## Intro (about 15 seconds)

Hi everyone. I built a program in C++ that reads farm data from a CSV file and gives reports about profits. The data comes from the game Stardew Valley. It has 224 days of farm records. Let me walk you through the code and the output.

## Part 1: The Code (about 60 seconds)

My program has two main classes.

The first one is called **FarmRecord**. Think of it like one row of data. It stores things like the year, the season, how many crops were sold, crop revenue, livestock revenue, expenses, and the net profit. It also has simple getter functions so other parts of the code can read these values.

The second class is called **FarmAnalyzer**. This is the brain of the program. It keeps a vector that holds all the farm records. It has four main jobs.

First, **loadData**. It opens the CSV file, skips the header line, reads each row, and splits it by commas. Then it turns the strings into numbers and adds a new FarmRecord into the vector.

Second, **generateProfitBySeasonReport**. It loops through every record, adds up the profit for each season, and divides by the number of days to get the average.

Third, **generateCropVsLivestockReport**. It adds up all crop revenue and all livestock revenue, then calculates what percent comes from crops.

Fourth, **getRecommendation**. It finds which season has the highest average profit and tells the user to focus on that season next time.

Finally, there is a **showMenu** function that keeps asking the user what they want to do, until they press 4 to exit.

## Part 2: The Output (about 45 seconds)

When I ran the program, it said "Loaded 224 farm records successfully." That means the CSV file was read correctly.

Then it showed a menu with four options.

I picked option 1, the Profit by Season Report. It told me that Spring averages $3,223 per day, Summer averages $3,538, Fall averages $3,178, and Winter averages $3,494. Every season had 56 days of data.

Next I picked option 2, the Crop vs Livestock Report. The total crop revenue was $708,992 and the total livestock revenue was $104,632. So crops make up 87.1% of all the money. That means this farm mostly sells crops, not animal products.

Then I picked option 3, the Recommendation. The program looked at the averages and said: "Prioritize Summer season for maximum profit." Because Summer had the highest daily average of $3,537.

Finally I pressed 4 to exit and it said "Thank you for using the Farm Analyzer."

## Closing (about 15 seconds)

So in short, this program takes raw farm data and turns it into useful information. It tells you which season earns the most money, where your revenue is coming from, and what to focus on next year. Thank you for listening.
