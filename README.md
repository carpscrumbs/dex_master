# dex_master
IC test for dexes. Calculates mean, std dev, observation and t-stat for all measures of success


#################################################################################################################################
############################################ SUMMARY OF SECTOR IC TEST #######################################################################
#################################################################################################################################

### Step one <- creates date_tibble
########################################################## DATE_TIBBLE ##########################################################################################################
### Steo two <- loads, cleans, long formats, calculates change and adds change column, cleans whitespace, left joins to date_tibble, range of sector_metric_table_date
####################################### RANGE OF FOR EACH METRIC SECTOR_METRIC_TABLE_DATE ##########################################################################################################
### Step two.five <- full joins the metric tables into dex_table_date
######################################################### DEX_TABLE_DATE ##########################################################################################################
### Step three <- formats long the dex_price csv, cleans the dex_price csv, calculates change over following month, left joins to date and creates dex_RONX_table_date
##################################################### SECTOR_RONX_TABLE_DATE ##########################################################################################################
### Step four <- join dex_table_date and dex_RONX_table_date to get full_dex_table
###################################################### FULL_SECTOR_TABLE ##########################################################################################################
### Step five <- calculate ranks and create dex_table_ranks using full_dex_table
####################################################### DEX_TABLE_RANKS ##########################################################################################################
### Step six <- calculate the correlation of ranks of each metric to RONX ranks. filter for just columns with corr and get dex_table_corr_date_only
################################################## DEX_TABLE_CORR_DATE_ONLY ##########################################################################################################
### Step seven <- use dex_table_corr_date_only and calculate cumulative sum of each metric, filter for only columns with cum in the column header sector_cum_only
###################################################### SECTOR_CUM_ONLY ##########################################################################################################
### Step eight <- Calculate the mean, std dev, obs, tstat for all the metrics, summarize and put in one table called combined_summary_stats_long
################################################### COMBINED_SUMMARY_STATS_LONG ##########################################################################################################
