import pandas as pd
import plotly.express as px

# Load your data
data = pd.read_csv('/Users/lucarossetti/Downloads/FAOSTAT_data_en_1-7-2024.csv')

# Create an interactive map using Plotly with a default color scale
fig = px.choropleth(
    data, 
    locations="Area", 
    locationmode="country names",
    color="Value", 
    hover_name="Area", 
    animation_frame="Year",
    color_continuous_scale=px.colors.sequential.Plasma,  
    projection="natural earth",
    title="Temperature Change by Country Over Years",
    range_color=[-1, 2.5]  
)

# Update layout to add a slider for years and improve map aesthetics
fig.update_layout(
    geo=dict(showframe=False, showcoastlines=False),
    margin={"r":0,"t":0,"l":0,"b":0}
)

fig.show()
