# Assessment_Taylor

####**1. How many markets sell items that are not edible?**
My first step was to exclude all markets that are located in a city(_E_) with the same name as the county(_F_) it is located in.  
My equation for this purpose was: =IF(E2=F2,"Y","N")  
My Next step was to identify which columns were labeled as non-edible items.  
There was a total of six columns that were non-edible,  including, crafts(_AA_), flower(_AB_), nursery(_AK_), plants(_AM_), soap(_AP_), and trees(_AQ_). I then created an equation to identify if a market sold any of these items.   
**IF** the market sells crafts **OR** flowers **OR** nursery items **OR** plants **OR** soap **OR** trees **THEN** the statement is "TRUE"  
My equation was: =OR (AA2="Y",AB2="Y",AK2="Y", AM2="Y",AP2="Y",AQ2="Y") 

Now I needed to combine the two conditions.  

**IF** the market did not have the same name as it's county **AND** sold at least one non-edible product **THEN** "TRUE"  
My equation looked like this: =AND(AT2="N", AV2=TRUE)
Finally I needed an equation to calculate the total amount of true statements in the column I had created (_AW_).  
My final equation was: =COUNTIF (AW2:AW8145,"TRUE") **The result was 3624 markets.** 

####**2. How many farmers markets could you visit in your home state where you could acquire all of the necessary ingredients to make your favorite meal?**  
My favorite meals these days is Coq Au Vin. This dish requires  herbs, vegetables, chicken and red wine. My sleepy seaside hometown is in the state of Connecticut. I looked at each column that corresponded with the ingredient I would need.  
1. _AE_: Herb  
2. _AF_: Vegetables  
3. _AN_: Poultry  
4. _AR_: Wine 

Then I looked at which column represented the state that the farmers markets was located.   
_G_: State

I needed to find out **IF** the market sells herbs **AND** vegetables **AND** poultry **AND** wine **AND** is located in Connecticut **THEN** it is true that I can go to the market to make Coq Au Vin. 

My equation on excel looked like:  =AND(AE2="Y",AF2="Y", AN2="Y",AR2="Y",G2="Connecticut")

Finally, I had  to find out the number of true statements so at the end of the column(AX).  
I formatted the equation: =COUNTIF (AX2:AX8145,"TRUE")  
This equation includes the entire range of Farmers Markets that I sorted through. **My results were only 2 markets!**

####3. How many markets are within the Oregon Territory area?

The column that represents the state the Farmers Market is located in is column G. I needed to make an equation that represented this statement: **IF** the market is located in Oregon **THEN** the statement is "TRUE"

My equation was =IF(G2="Oregon",TRUE,FALSE)

I then inserted an equation at the end of the column(_AZ_) to account for all the Truths.  
The equation I used to find my final answer was: =COUNTIF (AZ2:AZ8145,"TRUE") **The total amount of markets located in Oregon is 127.** 

####4.) What is one unique fact or pattern about farmers markets in the United States that you can recognize using the raw data?

There are 187 Farmers markets located at a faith-based institution (e.g., church, mosque, synagogue, temple). I decided to create an equation to find out if the majority of the Farmers Markets located at faith-based institutions are in southern states. 101 of the faith-based Farmers Markets are located below the latitude of 39.707957 or Mason Dixon Line. However, out of the 3729 Farmers Market in that area only 2.7 percent are located at faith-based buildings. Above the Mason Dixon Line 1.9 percent are located at faith-based buildings. I also thought it was interesting that out of the 110 farmers market located on a farm from: a barn, a greenhouse, a tent, a stand, etc only 40 of them were located bellow the Mason Dixon Line. Out of the 1395 Farmers Markets hosted at a Government Building, 607 are located bellow the Mason Dixon Line. It seems that even in agricultural-based areas of United States Farmers Markets are located away from the farm and faith-based communities and are featured in municipal areas.    
