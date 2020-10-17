# More About DataFrames

DataFrames are internally like 2D dictionaries, where you can access a specific cell by column and index, or row and index.

They're powerful structures that allow you to manipulate data just as fast or even faster than Excel. They also speak Excel, allowing you to go from DataFrame to and from spreadsheet pretty easily.

# How Element-Wise Operations Work

Internally, whem you do things like `max()` and `min()`, Pandas uses element-wise operations on a column, meaning it goes through every single value in that column automatically and creates a new column with the values, which you can keep separate or add it to the table.

# How `.loc` Works

How the `.loc` method works is that `price_history['Diff'] == max_diff` generates a new table with just True and False values, which `.loc` uses as a condition to indicate whether or not the particular row should be included within the result set. It then returns the rows that match.