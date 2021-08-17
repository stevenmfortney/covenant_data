# covenant_data

This repository contain collected data on syndicated lending covenants used in "Composition Risk: How Debt Structure Impacts Debt Contracting" by Steven Fortney (2021) and "Affirmative Covenants and Information-first Monitoring: Evidence from Syndicated Lending" by Steven Fortney (2021). Data is compiled by scraping syndicated lending agreements from SEC EDGAR and applying a novel textual analysis technique which I call Title-Recombination K-Means (TRKM) to each agreement. Full details of the TRKM technique are described in "Composition Risk: How Debt Structure Impacts Debt Contracting" (availible at stevenfortney.com). This readme only covers a brief overview of the datasets, for full details, a description of all fields, summary statitics and checks on the quality of the data, see the above papers. 

The repository contains two datasets. A dataset on negative covenants and a dataset affirmative covenants.

# Negative Covenants 

The first dataset https://github.com/stevenmfortney/covenant_data/blob/main/neg_loan_covs_matched_fisd_dealscan.csv is a dataset of 16 categories of negative covenants commonly found in syndicated lending agreements as identified by my TRKM methodology. Importantly, this dataset covers capital restrictions covenants which are not covered by existing publicly availible commercial databases. These include restrictions on actions such as the sale of unsecured assets, investments in entities outside of the credit group, merging with another entity, modifying liens or transacting with affiliates, to name a few. Each of the covenant cateories is chosen to match a corresponding class of covenant which are also found in bond indentures (as identified in Mergent's FISD database). One observation in the dataset corresponds to one syndicated lending agreement and the lending package it governs. For convenience, each observation is also matched to a lending package in the popular LPC DealScan database. These can be idenitified by the 'PackageID' field which can be directly matched over to data from LPC DealScan.    


# Affirmative Covenants 

The second dataset https://github.com/stevenmfortney/covenant_data/blob/main/aff_loan_covs_matched_dealscan.csv covers the 20 most commonly-used affirmative covenants in syndicated lending contracts as identified by my TRKM methodology. These covenants specify actions that borrowers must always take. As I discuss in "Affirmative Covenants and Information-first Monitoring: Evidence from Syndicated Lending", affirmative covenants are typically employed to make sure that banks can extract information from their borrowers and that the information they do extract is accurate to the current state of the firm. One observation in the dataset corresponds to one syndicated lending agreement and the lending package it governs. For convenience, each observation is also matched to a lending package in the popular LPC DealScan database. These can be idenitified by the 'PackageID' field which can be directly matched over to data from LPC DealScan.
