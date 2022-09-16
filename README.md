# VizTool NeuraFutures

NeuraFutures Data Analaysis & Visualization Tool allows users to explore connections betewen items in any kind of database. The tool casts rich statical and semantic data into an embedding space and allows users to explore dimensions along which they want to visualize connections.

Examples of embedding space dimensions include semantics (text and natural language meaning), date / time, location, and other calculated metrics.

---
## Database Structure

This software works for any data with a generic item-property schema:
| Item Title | Property #1 | Property #2 | Property #n |
| ---- | ---- | ---- | ---- |
| ... | ... | ... | ... |

---

## Setup
1. ```git clone``` repository url
2. ```pip install --upgrade -r requirements.txt```
3. ```cd app```
4. ```python -m streamlit run ABOUT.py```

## Usage

1. Download the most recent NeuraFutures database from the [notion page](https://www.notion.so/140058b1791b419894779170b29d1271?v=ce87848b9d4741b4b7ed4b310334d032).
2. (optional, only if database has changed in structure since 9/2022) Pre-process your data to make sure it is in a supported format.
3. Upload your database in the START page.
4. (optional) Put your images from the downloaded database folder (.jpg, .jpeg, and .png files only) into a folder and zip it. Upload this zip in the START page.
5. Explore the NETWORK, SEMANTICS, GRAPH, COMPARISON, and STATISTICS pages to analyze and visualize your data.

## Pre-processing
Pre-processing for NeuraFutures is handled automatically by the application. If the column values have chanegd since 9/2022, however, you may need to pre-process the data yourself. To do so:
1. Make sure you have an ID (by index) and TITLE column for each item in your database.
2. If you have a DATE column, make sure it is in an acceptable date format (e.g. YYYY).
3. Make sure all data within each column is formatted consistently.
4. If you have images in your database, load all images into the app/imgs folder and make sure the paths in your database correspond to the image file names.
5. The START page will guide you through labeling your database columns. You will add a prefix to each column header to indicate what type of data the column contains. The labels are as follows:
    * id - ID column
    * title - TITLE column
    * date - DATE column
    * img - image column
    * quant - quantitative data to analyze
    * sem - semantic data to analyze
    * cat - categorical data to analyze
    * info - additional information about the item, not analyzed

Your processed database should look something like this:
| [id] ID | [title] TITLE | [date] DATE | [img] Cover Image | [quant] Property #1 | [sem] Property #2 | [quant] Property #3 | [cat] Property #4 | [info] Property #5 |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| ... | ... | ... | ... | ... | ... | ... | ... | ... |

---

## Pages
* START - Load your database and preprocess it.
* NETOWRK - Explore connections between items in your database using a shared embedding space.
* SEMANTICS - Explore semantic properties of items in your database.
* GRAPH - Visualize correlations in your data using various types of graphs.
* COMPARISON - Compare and find similar items in your database.
* STATISTICS - Perform statistical analyses on your data.