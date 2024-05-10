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

<div align="center"><img src="" /></div>

