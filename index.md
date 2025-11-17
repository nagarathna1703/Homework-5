<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

# Altair & Vega-Lite Visualizations
Nagarathna Hosagoudar

---

## Visualization 1 — Building Usage Types in Top 10 Illinois Counties
Visualization 1 - Building Usage Types in Top 10 Illinois Counties by Number of State-Owned Buildings

This visualization shows the distribution of state-owned buildings across the top ten Illinois counties with the most facilities, with each bar representing a county and the stacked colored segments indicating the number of buildings in each usage category (such as Health Care, Education, Industrial, Residential, etc.). I used a stacked bar chart because it clearly communicates both the total number of buildings (encoded on the y-axis) and the composition of usage types within each county (encoded through color). Counties are placed along the x-axis as nominal values, while the y-axis represents the quantitative building counts. Color is mapped to the usage variable using a categorical palette so that each usage type is visually distinct and easily comparable across counties. Before creating the plot, I cleaned the dataset by selecting relevant columns, renaming them for clarity, removing missing or invalid county, year_built, floor_area, and usage entries, and filtering out unrealistic records. I then grouped the data by county to identify the top ten counties and grouped again by county and usage to compute the counts used in the stacked bars.

<div id="plot1"></div>
<script>
vegaEmbed('#plot1', 'plot1.json');
</script>

---

## Visualization 2 — Construction Year Distribution by Status (Interactive by County)
Visualization 2 - Construction Year Distribution by Status (Interactive by County)

This visualization shows how the construction years of state-owned buildings are distributed within each Illinois county and how these buildings differ by operational status. Each bar represents a ten-year construction window, and the stacked colored segments indicate how many buildings within that decade fall into each status category, such as “In Use,” “In Progress,” or “Abandon.” I used a stacked histogram because it effectively communicates both the overall construction activity (encoded on the y-axis) and the breakdown of building statuses within each decade (encoded through color), while the x-axis displays construction years binned by decade to make long-term patterns easier to interpret. Color is mapped to the status variable using a nominal palette so that each status category is visually distinct and interpretable across bins.


<div id="plot2"></div>
<script>
vegaEmbed('#plot2', 'plot2.json');
</script>

---

## Interactivity Discussion
Interactivity in the visualization - I added a dropdown selector in Altair that allows viewers to choose a specific county, dynamically updating the histogram to show how construction trends and building statuses vary by region. This interactivity makes the visualization more engaging and clearer by enabling users to focus on one geographic area at a time rather than interpreting a combined statewide distribution.


---

## Links

### 🔗 The Data  
[Building Inventory Dataset](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)

### 🔗 The Analysis Notebook  
[Workbook.ipynb](Homework5.ipynb)
