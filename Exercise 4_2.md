# Week 4 – Exercise 2 Cleaning Data

As the saying goes, “garbage in, garbage out.” If your data are not accurate, whether because of mistaken observation at the time of recording or because of a simple mistake in transcribing the information, they will not be very useful in the future. It is obviously important to be careful when you’re enter data, but we’re all human (i.e. not perfect) and mistakes happen. Before you start using your data to say meaningful things about the archaeological past, it is therefore important to make sure your information is standardized and as “clean” as it can be. There are manual ways to do this, which are time consuming. There are also software available that make identifying irregularities in your data easy and allow you to spend less time looking for mistakes. 

An extremely useful tool for this is called OpenRefine – a free, open source tool for working with messy data ([their words](http://openrefine.org/)).  
1.	Make sure OpenRefine is downloaded and installed on your local machine. If it is not, let your instructor know. 
2.	We’re next going to find the data we’ll work with to “clean.” Check out the Petra Great Temple Excavations data published on Open Context [here](https://opencontext.org/projects/A5DDBEA2-B3C8-43F9-8151-33343CBDC857). Read the background to the project given in the project abstract. These excavations produced many different types of data, some of which you can see at the bottom of the project page under “Related Data Tables for Download.” 
3.	We will use two different data tables to test out our skills in database cleaning using OpenRefine. First, click on the table titled “Petra Great Temple Excavation Trenches.” On the next page, click on the blue button on the top right corner of the page, Download CSV. Note a folder on your local hard drive where you are downloading this file to and name it “Petra Excavation Trenches Data.”
![alt text](https://github.com/kgarstki/ANTH-641_Week-4/blob/master/Images/Image1.png)
4.	Repeat the same process for the data table titled “Petra Great Temple Pottery” and name the file “Petra Pottery Data.” And repeat the same process for the data table titled “__Petra Great Temple Animal Bones__” and title it “__Petra Animal Bones__.”
5.	Click on the openrefine application that is downloaded on your hard drive. 
![alt text](https://github.com/kgarstki/ANTH-641_Week-4/blob/master/Images/Image2.png)
6.	This will open your internet browser – while OpenRefine uses Chrome as its interface, it does not transfer your data to an external server (it remains safe on your own device). Click on the Choose Files button and find your “Petra Excavation Trenches Data” file and load it into OpenRefine by clicking “Next >>”
![alt text](https://github.com/kgarstki/ANTH-641_Week-4/blob/master/Images/Image3.png)
7.	On the next page, you simply need to click “Create Project >>” on the top right corner of the page. 
8.	Now that your data is loaded into a project in OpenRefine, watch [this short](https://www.youtube.com/watch?v=B70J_H_zAWM) introduction to the program. 
9.	The main thing we are going to focus on are discrepancies in the data within a single field. You may be entering information quickly when you’re in the field or in the lab and this may cause you (or someone else) to mistype something. In other cases, two or more people may be entering data and not have a standardized way to input certain information. This tool can help mitigate some of those mistakes and make the data more useable. To begin, in your Petra Excavation Trenches Data project, scroll over to the field called “Context (4)” and click the dropdown arrow. Under “Facet” click on Text Facet. 
![alt text](https://github.com/kgarstki/ANTH-641_Week-4/blob/master/Images/Image4.png)
10.	This will bring up a box on the left side of your screen that groups all of the different types of entries in this field, with a small number next to the text that represents how many times each are used in the database. For example, Grid C- 3 is used one time, and None is used nine times. 

![alt text](https://github.com/kgarstki/ANTH-641_Week-4/blob/master/Images/Image5.png)

11.	We could go through this list of 269 choices manually and look for redundancies, or we can ask the program to look for us. If you click on the “Cluster” button on the top of the Context (4) section, you will see that OpenRefine grouped similar text entries into single groups. In this case, it seems that many of the “Special Project” labels included an extra space in between Project and the Number. One space…that’s how easy it is to make a mistake that affects the usability of an entire data record!

12.	We can combine these cell values together so that these mistaken entries won’t cause us problems in their future use. Click on the box in the Merge? column for the Special Project clustered values. Then click on Merge Selected & Re-Cluster at the bottom of the screen. 

![alt text](https://github.com/kgarstki/ANTH-641_Week-4/blob/master/Images/Image6.png)

13.	You will now see that those clusters are gone from your list of clusters. The only cluster that remains is a cluster of two: Trench 69 and Trench 69? Should we merge these two values? The answer is probably not – it appears that the recording strategy at this excavation was to build in uncertainty into the records. Whoever was entering this data may not have known if this was supposed to be Trench 69 or not. This is not an ideal situation for this data, but we’d have to do some additional digging through the data and excavation notes to understand why this choice was made and to be comfortable changing the data. Use this as an opportunity to think about how little choices during data recording can affect the long-term use of archaeological datasets. 

14.	Close the cluster and edit box and return to manually scrolling through the Context (4) filter on the left side of the screen – can you find any other issues or discrepancies? Think about what are the best ways to make those changes to clean the data and go ahead and edit the information. In your README.md file in your ANTH 641_Week 4 repo, __write__ out the __changes__ you made in this dataset. 

15.	Next go back to the main project data table and choose to look at the Text Facet from the column “Label.” Once again, look at the clusters that OpenRefine generates for you. What are some of the issues you see with different recording in these clusters? What are some changes that you made in grouping these data values together and what are clusters that you had to leave how they were? Again, __note__ in your README.md file what you’ve changed. 

16.	When you’ve cleaned these two fields (Context (4) and Label), export the project as Petra Excavation Data_Cleaned. Go to your GitHub page and create a new repo titled “ANTH 641_Week 4.” Upload your cleaned .xlsx file to your Week 4 GitHub page.

17.	Next, begin a new project by clicking on the “Open…” button on the top right of the page. Load your Petra Animal Bones csv file. 

18.	Now that you know how to look for and standardize data fields, clean the fields “Common Name” and “Element.” Export the project as Petra Animal Bones_Cleaned to a known place on your computer and upload it to this week’s GitHub repo. In your README.md file in your ANTH 641_Week 4 repo, __write__ out the __changes__ you made in this dataset.

19.	Finally, load Petra Pottery Data file into OpenRefine. When you begin to explore the data table, you’ll notice there isn’t much cleaning that needs to be done – fields are filled out fairly consistently across the table. However, scroll to the last column titled, “Description.” This description is taken from the ceramics report that can be viewed on Open Context [here](https://opencontext.org/media/83CA6A5A-3FDF-4F71-7C01-7CF023D1EA27). Will a field such as this help you were you to use these data for further analysis or comparison, why or why not? Think about what makes a useful field in a database or data table; what types of information can be used for larger scale analysis? You can elaborate on what you learned here in your blog post. 

20.	You won’t have edited anything on this file but upload it into your ANTH 641_Week 4 repository on GitHub so that you can access it later. 

