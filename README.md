Note: UnderStat website contains only league matches data, not UEFA Champions league or International matches.

This notebook contains a code scrapes the data for a single player from understat.com website, which provides a statistical data for the top 5 leagues from 2014/2015 season until now. You can scrape all the data you need by only passing the player id from the website, and then this notebook will do it all. To accomplish my work, I have used some sources I'll mention them lately.

To explain my code, I'll use the Egyptian king "Mohamed Salah" as an example:

![search tab](https://user-images.githubusercontent.com/80650976/184650011-dd52a99b-c14c-4246-b68c-b617a6173b8f.PNG)

After passing the player id, there are many functions to find and filter the data you want:

1- GetMatchesData():

 this function returns a csv. file contains all the matches played for this player in the top 5 leagues since 2014/2015 season with match details and the player performance in this match.

Scraped table from the website:

![matches data](https://user-images.githubusercontent.com/80650976/184649440-fec82eae-1a5c-4b33-835b-a17df75fd45f.PNG)

Output table:

![GetMatchesData](https://user-images.githubusercontent.com/80650976/184655271-aaacf896-6675-4e49-9d51-789ce3a70d5e.PNG)

2- PlayerSeasonStats():

This function focuses on a particular season entered by the user, and gives output as below:

![PlayerSeasonStats](https://user-images.githubusercontent.com/80650976/184655798-da90eabb-4e4e-45fe-a870-0648ddd59bbc.PNG)

3- PlayerCareerStats():

This function returns as csv. file with the summary statistics for every season like below:

![PlayerCareerStats](https://user-images.githubusercontent.com/80650976/184656718-8fa51b3d-ca54-43c0-b30d-1be0d1100827.PNG)

4- TabularShotsData():

This function scrapes the intetractive shotmap in the website and returns it in a csv. file:

![TabularShotsData](https://user-images.githubusercontent.com/80650976/184657884-bf8aa007-9e09-49f8-bb16-54285945c4f4.PNG)

5-  TimeTier():

This function filter the shots by the time interval, which was set for every 15 minutes. 

The output:

![TimeTier](https://user-images.githubusercontent.com/80650976/184658406-96ea5033-0923-4243-9ada-93781aef78b6.PNG)

6- xGTier():

This function filter the shots by the shot quality, which was set using the table below:

![xG Tier](https://user-images.githubusercontent.com/80650976/184651631-3151338c-c73d-4ab7-b355-9a644075694d.PNG)

The output:

![xG Tier](https://user-images.githubusercontent.com/80650976/184660645-7805218e-b3ca-405c-be1d-8dc9428ccc90.PNG)

7- ShotsArea():

This function returns a csv. file with the shot zones filtered by season.

The output:

![ShotsArea](https://user-images.githubusercontent.com/80650976/184661402-f8ec0729-1263-490c-8819-d50b6fc8458d.PNG)

8- PlotShots()

This function recreates the interactive shot map using mplsoocer package

![Mohamed Salah 1250](https://user-images.githubusercontent.com/80650976/187049314-74490e67-ba96-402a-94df-bab2d163ba28.jpg)

9- KeyPassers()

This function displays the top key passers for the player, and returns the output in a csv. file

The Output:

![keypassers](https://user-images.githubusercontent.com/80650976/184663075-bf75ff8c-2400-449c-b4ed-a470a77fd0b3.PNG)

10- KeyPassTypes()

This function displays the top key pass types, and returns the output in a csv. file.

The Output:

![KeyPassTypes](https://user-images.githubusercontent.com/80650976/184665108-7ca70ddb-5802-42c3-b80c-56c8fc9aa063.PNG)


Sources:

 * How to scrape Understat for football data in Python with requests and BeautifulSoup - McKay Johns (YouTube)
   https://youtu.be/IsR5FrjNmro
  
 * How to create football shot maps in python - McKay Johns (YouTube)
  https://youtu.be/2RhTuRWNqUc
 
 * mplsoccer package documentaion
  https://mplsoccer.readthedocs.io/en/latest/index.html#
 
 * من أين تأتي الأهداف؟ - سبورت 360 عربية(YouTube)
  https://www.youtube.com/watch?v=KOaJ6RFACrU
