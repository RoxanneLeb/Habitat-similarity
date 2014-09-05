# HRI & Impact Score (birds endemicity)
==================

**Objective** : to see where are the most "unic" area in Africa (according to environmental variables), and to see if there is a trend between these areas and forest birds endemicity

**Hypothesis** : habitat which are not similar to others would have more endemic species than common habitats

**M&M** : computing HRI using a moving window approach on African forested area

## I. Maps
###########

From worlwilde *impact_score* map : ext= worldwilde, res= 5 km, proj= longlat (Buchanan et al., 2011) :

Transformation (ArcGis) : ext= africa, res= 5km, proj= mollweider 

**Raster :**
* *Af_impact_score* : clip impact score map with *af_forest*

**Vector :**
* *af_forest* : forested area in Africa
* *af_forest_grid_50km* : grid of 50km in African forest used as window to compute HRI
* *af_ecoreg_forest* : ecoregion in forested area

## II- Computing HRI 
####################

Using Python and GRASS

Output = HRI computed for each polygon of 50km squared => raster maps

## III- Sum output keeping the highest HRI value
################################################

Replace NULL values by 0 (to do stats on the layer and take the highest value)

Final map adding all the rasters keeping the max value


