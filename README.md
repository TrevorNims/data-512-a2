# data-512-a2

This exploration will explore the concept of bias through data on Wikipedia articles - specifically, articles on political figures from a variety of countries. Within the notebook, we will combine a dataset of Wikipedia articles with a dataset of country populations, and use a machine learning service called ORES to estimate the quality of each article. Next we will perform an analysis of how the coverage of politicians on Wikipedia and the quality of articles about politicians varies between countries by examining a series of generated tables.

The source data is contained in the data directory, and consists of two files:

  1. **page_data.csv** which is a csv file containing information on politicians' wikipedia pages by country. The dataset can originally be found on figshare: https://figshare.com/articles/Untitled_Item/5513449

  2. **WPDS_2020_data - WPDS_2020_data.csv** which is a csv file containing population data for countries/sub-regions referenced in the **page_data.csv** dataset.        This dataset is drawn from the world population data sheet published by the Population Reference Bureau: https://www.prb.org/international/indicator/population/table/

To apply the Machine Learning model to predict page rankings, we will utilize the ORES API (documentation: https://ores.wikimedia.org/v3/#/), this can also be done by installing the ORES package (Github Repo: https://github.com/wikimedia/ores).

The data folder also contains a few intermediary .csv files:

  1. **unscorables.csv** a csv file containing article reference ids that were not able to be scored by the ORES model.
  2. **wp_wpds_countries-no_match.csv** a csv file containing articles that did not match any country in the **WPDS_2020_data - WPDS_2020_data.csv** file.
  3. **wp_wpds_politicians_by_country.csv** a csv file containing all articles and their article rankings as given by the ORES model.
