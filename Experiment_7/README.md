# Experiment 7: Handling Overplotting in Visualization

## Description
This experiment addresses the challenges of visualizing large or dense datasets, specifically the problem of **overplotting**. It demonstrates techniques to reveal hidden patterns and data density that are obscured when many data points overlap. The analysis uses social media interaction data (Likes vs. Shares).

## Files Included
*   `code/ex7.R`: R script demonstrating three distinct overplotting reduction techniques.
*   `data/7.social_media_interactions.csv`: Dataset containing social media engagement metrics (`Likes`, `Shares`).
*   `figures/`: Directory for output visualizations.

## Visualization Outputs
1.  **Alpha Blending (Transparency):**
    *   **Technique:** Modifying the opacity (alpha channel) of data points.
    *   **Objective:** To reveal high-density areas where points overlap by making darker regions correspond to higher data concentration.

2.  **Jittering (Noise Addition):**
    *   **Technique:** Adding small amounts of random noise to the data coordinates.
    *   **Objective:** To separate perfectly overlapping points (often caused by discrete data or low precision) to show the true volume of data.

3.  **Aggregation (Density Heatmap):**
    *   **Technique:** Using `smoothScatter` to estimate local data density.
    *   **Objective:** To visualize the overall distribution shape and hotspots using a color gradient (White -> Cyan -> Blue).

## Methods Used
*   Standard Scatter Plot with `rgb(alpha)`
*   `jitter()` function
*   `smoothScatter()` function

## Dependencies
*   Base R Graphics
*   `ggplot2` (Loaded for environment setup)
*   `scales`
