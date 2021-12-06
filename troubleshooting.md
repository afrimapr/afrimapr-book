# Troubleshooting

We provide a list of typical errors that may appear as you work in R or use it for map-making purposes. They come from our experience when working on the book and some of them are borrowed from other sources, for example, [The Epidemiologist R Handbook](https://epirhandbook.com/en/common-errors.html).

## Packages

- When installing the package, error in install.packages : object 'x' not found.
    - Usually quotation marks are missing, e.g. install.packages("x")
- When loading the package, there is no package called 'x' 
    - The required package is not yet installed.
- Could not find function "x"
    - Package is missing, install and load required package.

## Typos
 
- The ' unexpected symbol' error in the map making code.
    - The is a typo or missing comma.

## Objects

- object 'x' not found 
    - Suggest that object x does not exist in the environment. Double-check if you reference correctly to it. E.g. if the spelling is correct or the object is contained within the dataset (dataset$x)
   

## Plotting and visualisaions

- A map is incomplete/ does not appear.
    - Map-making code does not fully run, potentially there is a missing + after last ()
- "Error in ...: figure margins too large"    
    - Increase the size of a plot pane to fit the map.
- Some legend labels were too wide. 
    - Increase legend.width (argument of tm_layout) to make the legend wider.
- Error: Discrete value supplied to continuous scale    
    - Convert the factor variable (discrete) to numeric to be able to plot it as continuous.
- Insufficient differentiation in default brakes for map to be readable.
    - Set up custom brakes, for more guidance please refer to section 5.3 in our book.