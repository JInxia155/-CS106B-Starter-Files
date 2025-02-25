Download Link : https://programming.engineering/product/starter-files/

# CS106B-Starter-Files
Starter Files
Each student begins with four late days that may be used throughout the quarter. You may submit this assignment 24 hours late by using one late day or 48 hours late using two late days. No submissions will be accepted more than 48 hours after the due date without prior approval by the head TA. See the syllabus for more information about our late policies.

All due dates and submission times are expressed in Pacifc time.

This assignment must be completed individually. Working in groups is not permitted.

This assignment is all about the amazing things you can do with collections. It’s a two-parter. The frst is a program that can guess the language a piece of text is written in. The second models rising sea levels on a sampler of realistic terrains. By the time you’ve completed this assignment, you’ll have a much better handle on the container classes and how to use diferent types like queues, maps, vectors, and sets to model and solve problems. Plus, you’ll have some things we think you’d love to share with your friends and family.

This assignment has two parts. It will be quite a lot to do if you start this assignment the night before it’s due, but if you make slow and steady progress on this assignment each day you should be in great shape. Here’s our recommended timetable:

Aim to complete Rosetta Stone within four days of the assignment going out.

Aim to complete Rising Tides within seven days of this assignment going out.

As always, feel free to reach out to us if you have questions. Feel free to contact us on EdStem, to email your section leader, or to stop by the LaIR.

Assignment Logistics

Starter Files

We provide a ZIP of the starter project. Download the zip, extract the fles, and double-click the .pro fle to open the project in Qt Creator.

                    		
                    					
                    					
                    		
                    		
                    		
                    		
                    		
                    		

                		
                		
                		
                		
                		
                		
                	
                		
                		
                		
                		

		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		

                    		
                    		
                    				
                    		
                    				
                    		
                    		
                    			
                    			
                    				
                    			
                    			
                    			
                    				
                    					

			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			
			

                		
                		
                		
                		
                		
                		
                		
                		
                		
                		

		
		
		
		
		
		
		
		
		
		
		
		
		
		
		

                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		
                		

                    	
                    	
                    			
                    		

                					
                								
                			
                							
                				
                								
                				
                				
                							
                	
                				
                	
                				
                			
                		
                				

2023/3/25 17:28 CS106B Fun with Collections

Answer the following question in the fle ShortAnswers.txt:

Q5. In Q4 of this problem you proposed three ways in which you could use additional time and resources to improve your testing regimen. If you had to select only one of them, which one would you pick, and why? In writing your answer, please address the following:

What are the advantages of picking the approach you selected compared with the other two approaches? What are the disadvantages?

What are the advantages of picking the other two approaches? What are the disadvantages?

Based on your analysis, why do you think it is best to select the approach you did?

Your answer should be 5 – 10 sentences in length.

Thank you for working through this exercise. If you are interested in exploring more of the tradeofs involved here, we invite you to think about the following.

    In the scenario described above, your tool was to be used for content moderation on a social media website that had not yet launched. However, suppose you were instead adding moderation to an existing social media site. How would you balance the benefts and harms associated with rolling out an imprecise content moderation tool with the benefts and harms of delaying the rollout of the tool until it had been improved and polished?

        In practice, your tool may face a tradeof in which it can either identify a smaller number of languages more precisely or a larger number of languages less precisely. What impact might this have if you tool was used in the context of content moderation? What benefts and harms may arise in each case? Who would be impacted, and how would you decide which approach to take?

    You aren’t expected to submit anything in response to these last two questions, though you are welcome to come and chat with us about them if you are interested!

    Part Two: Rising Tides

    Background: Our Model

    Global sea levels have been rising, and the most recent data suggest that the rate at which sea levels are rising is increasing. This means that city planners in coastal areas need to start designing developments so that an extra meter of water doesn’t food people out of their homes.

    Your task in this part of the assignment is to build a tool that models fooding due to sea level rise. To do so, we’re going to model terrains as grids of doubles, where each double represents the altitude of a particular square region on Earth. Higher values indicate higher elevations, while lower values indicate lower elevations. For example, take a look at the three grids to the right. Before moving on, take a minute to think over the following questions, which you don’t need to submit. Which picture represents a small hill? Which one represents a long, sloping incline? Which one represents a lowland area surrounded by levees?

    Due Friday, at 1:00 pm

    Assignment Logistics Part One: Rosetta Stone

    Background: Trigrams

    Background: UTF-8

    Milestone One: Form k-Grams

    Milestone One Requirements

    Milestone Two: Normalize Frequen

    Milestone Three: Filter Out Uncom

    Milestone Four: Implement Cosine

    Milestone Five: Guess a Text’s Lan

    Milestone Six: Explore and Evalua

    Milestone Seven: Ethical Considera

    Part Two: Rising Tides

    Part Three: (Optional) Extensions Submission Instructions

    2023/3/25 17:28 CS106B Fun with Collections

    Due Friday, at 1:00 pm

    Assignment Logistics

    Part One: Rosetta Stone

    Background: Trigrams

    Background: UTF-8

    Milestone One: Form k-Grams

    Milestone One Requirements

    Milestone Two: Normalize Frequen

    Milestone Three: Filter Out Uncom

    Milestone Four: Implement Cosine

    Milestone Five: Guess a Text’s Lan

    Milestone Six: Explore and Evalua

    Milestone Seven: Ethical Considera

    Part Two: Rising Tides

    Part Three: (Optional) Extensions

    Submission Instructions

    Notice that the water overtops the levees in the central world, completely fooding the area, as soon as the water height reaches three meters. The water line never changes, regardless of the current elevation. As such, water will never food across cells at a higher elevation than the water line, but will food across cells at the same height or below the water line

    Your task is to implement a function

    Grid<bool> floodedRegionsIn(const Grid<double>& terrain,

    const Vector<GridLocation>& sources,

    double height);

    that takes as input a terrain (given as a Grid<double>), a list of locations of water sources (represented as a Vector<GridLocation>; more on GridLocation later), and the height of the water level, then returns a Grid<bool> indicating, for each spot in the terrain, whether it’s under water (true) or above the water (false).

    You may have noticed that we’re making use of the GridLocation type. This is a type representing a position in a Grid. You can create a GridLocation and access its row and column using this syntax:

    GridLocation location;

    location.row = 137;

    location.col = 42;

    GridLocation otherLocation = { 106, 103 }; // Row 106, column 103 otherLocation.row++; // Increment the row.

    cout << otherLocation.col << endl; // Prints 103

    Background: Breadth-First Search

    Now that we’ve talked about the types involved here, let’s address how to solve this problem. How, exactly, do you determine what’s going to be underwater? Doing so requires you to determine which grid locations are both (1) below the water level and (2) places water can fow to from one of the sources.

    Fortunately, there’s a beautiful algorithm you can use to solve this problem called breadth-frst search. The idea is to simulate having the water fow out from each of the sources at greater and greater distances. First, you consider the water sources themselves. Then, you

    https://web.stanford.edu/class/archive/cs/cs106b/cs106b.1234/assignments/a2/ 21/21

