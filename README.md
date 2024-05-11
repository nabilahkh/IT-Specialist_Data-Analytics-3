# DATA VISUALIZATION

Data visualization is the representation of data through the use of common graphics, such as charts, plots, infographics, and even animations. These visual displays of information communicate complex data relationships and data-driven insights in a way that is easy to understand.

Matplotlib and Seaborn are Python libraries that are used for data visualization. They have built-in modules for plotting different graphs. While Matplotlib is used to embed graphs into applications, Seaborn is primarily used for statistical graphs.

### Basic Visualization

1. Bar Chart Vertical
   Compare among categories, few categories. Can be used over time
2. Bar Chart Horizontal
   Has a long item label. Compare among categories. Used for many categories
3. Line Chart
   Compare over time, one category
4. Stacked Bar Chart
   Show components in a category, that can be used over time(a few periods). Relative and absolute differences matter.
5. Stacked 100% Bar Chart
   Show components in a category. Composition in percentage, focus contribution on each component. Can be used over time (a few periods) and only relative differences matter.
6. Pie Chart
   Static Composition, Useful for less than 5 categories. A simple share of the total
7. TreeMap
   Static Composition, accumulation to total. Absolute difference matters

### Data Visualization Using Python
Python offers several plotting libraries namely Matplotlib and Seaborn for data visualization.

#### • Matplotlib
1. It used for basic graph plotting
2. It mainly works with dataset and array
3. Matplotlib acts productively with data arrays and frame
4. Matplotlib is more customizable and pairs well with Pandas and Numpy

   
#### • Seaborn
1. It mainly used for statistics and complex visualization
2. It works with the entire dataset
3. More organized and functional than Matplotlib, the dataset as a solitary unit
4. Seaborn has more themes and statistical analysis.

##### Import matplotlib and seaborn
                                                import matplotlib.pyplot as plt
                                                %matplotlib inline
                                                import seaborn as sns
                                                
##### Creating variables
Creating two variables to display a chart

                                                years = [2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023]
                                                yield_grapes = [0.90, 1.00, 1.10, 1.20, 1.30, 1.40, 1.55, 1.67]

Displaying a chart from the previously created variables                                     

                                                plt.plot(years, yield_grapes) #plt.plot(x, y)
                                                
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/3ef2020f-2d3c-4168-bf3a-07035460da16" /></div>

##### Creating labels
Adding one variable for the Y-axis, still with the same category, which is fruits

                                                grapes = [0.90, 1.00, 1.10, 1.20, 1.30, 1.40, 1.55, 1.67]
                                                kiwi = [0.50, 0.67, 0.47, 0.77, 1.07, 1.15, 1.27, 1.87]

Displaying a chart for the quantity of harvested grapes and kiwis in the specified year. Then, adding title labels to the X and Y axes.

                                                plt.plot(years, grapes)
                                                plt.plot(years, kiwi)
                                                plt.xlabel('Year')
                                                plt.ylabel('Yield (tons per hectare)');
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/a39da086-0792-4265-b2cb-98106d35e850" /></div>

##### Creating tittle and legend
Adding a title to the graph and a legend to indicate the graph based on color (Blue for grapes and Orange for kiwi)

                                                plt.plot(years, grapes)
                                                plt.plot(years, kiwi)
                                                
                                                plt.xlabel('Year')
                                                plt.ylabel('Yield (tons per hectare)');
                                                
                                                plt.title("Crop Yields in Kanto")
                                                plt.legend(['Grapes', 'Kiwi'])
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/e3e384a2-47f2-49da-874e-79b8dd70ef90" /></div>

##### Creating grid
An easy way to make your charts look beautiful is to use some default styles from the Seaborn library. These can be applied globally using the sns.set_style function.

Creating a visualization plot with a white background and grid.

###### - Whitegrid
                                                sns.set_style("whitegrid")
                                                
                                                plt.plot(years, grapes, marker='o')
                                                plt.plot(years, kiwi, marker='x')
                                                
                                                plt.xlabel('Year')
                                                plt.ylabel('Yield (tons per hectare)');
                                                
                                                plt.title("Crop Yields in Kanto")
                                                plt.legend(['grapes', 'kiwi'])
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/9d639f22-c7b3-423b-9aa3-884148b997c0)" /></div>

The syntax above is used to create a graph showing the yields of grapes and kiwi over the years. It sets the X-axis label as 'Year', the Y-axis label as 'Yield (tons per hectare)', and the title of the graph as 'Crop Yields in Kanto'. A legend is added to distinguish between the lines representing grapes and kiwi, with 'grapes' represented by circles (marker='o') and 'kiwi' represented by crosses (marker='x')

###### - Darkgrid
Creating a visualization plot with a dark background and grid.

                                                sns.set_style("darkgrid")
                                                
                                                plt.plot(years, grapes, marker='o')
                                                plt.plot(years, kiwi, marker='x')
                                                
                                                plt.xlabel('Year')
                                                plt.ylabel('Yield (tons per hectare)');
                                                
                                                plt.title("Crop Yields in Kanto")
                                                plt.legend(['grapes', 'kiwi'])
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/89d01558-f13e-4012-bb4c-fc80c0aff1ca" /></div>

##### Creating a Bar Chart
Creating a bar chart showing the grape yields from year to year in Bandung

                                                plt.bar(years, grapes)
                                                
                                                plt.xlabel('Year')
                                                plt.ylabel('Yield (tons per hectare)');
                                                
                                                plt.title("Crop Yields in Bandung")
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/0041827b-f2f8-4f9f-956a-83114b9928fc" /></div>

##### Creating a Stacked Bar Chart
Creating a stacked bar chart showing the grape and kiwi yields from year to year in Bandung. Grapes are represented by the first bar chart, while kiwi is represented by the second bar chart. The argument bottom=grapes sets the kiwi bar chart to start from the grape yields, thereby showing the comparison between the two yields for each year.

                                              plt.bar(years, grapes)
                                              plt.bar(years, kiwi, bottom=grapes)
                                              
                                              plt.xlabel('Year')
                                              plt.ylabel('Yield (tons per hectare)');
                                              
                                              plt.title("Crop Yields in Bandung")
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/2a168184-daa8-4333-9abd-71663278c55a" /></div>

### Data Visualization From Seaborn Library
The Seaborn library is a Python package that focuses on statistical data visualization. It serves as a high-level interface built on top of Matplotlib, providing a simpler and more efficient interface for creating appealing and informative statistical graphics

#### Creating Bar Chart
##### Import dataset 'glue' from Seaborn

                                             df = sns.load_dataset("glue")
                                             df.head()
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/dcada93d-86de-4082-b854-855ee5af0d1e" /></div>

##### Creating a bar plot
Creating a bar plot to represent the 'Model' column against the 'Score' column in the 'glue' dataset

                                             sns.barplot(x='Model', 
                                                         y='Score',
                                                         data=df)
                                             
                                             plt.xticks(rotation=45)
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/2564b364-1290-4b17-9ba9-a6955753a041" /></div>

Creating a bar plot by dividing it based on the values in the 'Year' column, thus displaying different colors for each year

##### Creating a bar chart vertical (pivot)
                                             sns.barplot(x='Model', 
                                                         y='Score',
                                                         hue='Year',
                                                         data=df)
                                             
                                             plt.xticks(rotation=45)
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/98da8a6b-bd24-45b1-a48e-d6c971b006bf" /></div>

##### Creating a bar chart horizontal (pivot)
                                             sns.barplot(x='Score', 
                                                         y='Model',
                                                         hue='Year',
                                                         data=df)
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/b2979478-91e8-447b-906e-4cbb1ac16818" /></div>

#### Creating Histogram
##### Import dataset 'flights' from Seaborn
                                             flights_df = sns.load_dataset("flights")
                                             flights_df.head()
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/33b61b14-c798-4677-b133-1adabf41d314" /></div>     

##### Creating histogram distribution With "Bins=7"
Create a histogram displaying the distribution of the number of passengers on flights, where the histogram result uses the number of passengers as input data and the argument bins=7 is used to determine the number of bins or data groups used in the histogram

                                             #We can control the number of size bins too 
                                             #specifying the number of bins
                                             
                                             plt.title("Distribution of Passengers")
                                             plt.hist(flights_df.passengers, bins=7);
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/43d2a5ac-e425-4b11-a6e8-02f71aa7cc0b" /></div>    

##### Creating histogram distribution With "Bins=100, 500, 10"
Displaying a histogram of the distribution of the number of passengers on flights using the argument bins=np.arange(100,599,10), which is used to explicitly determine the bin boundaries, starting from 100 up to 500 with an interval of 10.

                                             import numpy as np
                                             
                                             #specifying the number of bins
                                             plt.hist(flights_df.passengers, bins=np.arange(100,500,10));
                                             
                                             plt.title("Histogram of Passenger Counts")
                                             plt.xlabel("Number of Passengers")
                                             plt.ylabel("Frequency")
<div align="center"><img src="https://github.com/nabilahkh/IT-Specialist_Data-Analytics-3/assets/92252191/d7f7c6c9-e399-4b62-b14f-5c2a167068c3" /></div>                                              
### Crisp DM
The Cross-Industry Standard Process for Data Mining, or CRISP-DM, is one of the data mining process models.

**1. Business Understanding** – What does the business need?

**2. Data Understanding** – What data do we have/need? Is it clean?

**3. Data preparation** – How do we organize the data for modeling?

**4. Modeling** – What modeling techniques should we apply?

**5. Evaluation** – Which model best meets the business objectives?

**6. Deployment** – How do stakeholders access the results?
