# Google Ad Analysis SpotApp

SpotApps are ThoughtSpot’s out-of-the-box solution templates built for specific use cases and data sources. They leverage ThoughtSpot Modeling Language (TML) Blocks, which are pre-built pieces of code that are easy to download and implement directly from the product.

The Google Ad Analysis SpotApp mimics the Google Ads data model. When deployed, it creates several Worksheets, Answers, and Liveboards based on your Google Ads data in your cloud data warehouse.

This is a sample Liveboard, created after you deploy the Google Ad Analysis SpotApp:
![Google Ad Analysis SpotApp Liveboard](https://github.com/thoughtspot/Google-Ad-Analysis-SpotApp/assets/102629468/868052c6-5572-4658-8fed-d1ba40cbd604)

Use the Google Ad Analysis SpotApp to get invaluable insight into your Google Ads performance, from high-level usage to identifying popular campaigns.

## Prerequisites

Before you can deploy the Google Ad Analysis SpotApp, you must complete the following prerequisites:

- **Review Required Data**: Examine the required tables and columns for the SpotApp.
- **Ensure Column Compatibility**: Ensure that your columns match the required column type listed in the schema for your SpotApp.
- **Sync Data**: Synchronize all tables and columns from Google Ads to your cloud data warehouse. While you can choose to sync only the required tables and columns, ThoughtSpot recommends syncing all tables and columns from Google Ads to ensure comprehensive data availability. This includes Google Ads’s out-of-the-box columns or any custom columns you are using.
- **Collaborate on Data Movement**: If you are using an ETL/ELT tool or working with another team within your organization, sync all columns from the tables listed in the SpotApp.
- **Obtain Credentials**: Acquire credentials and SYSADMIN privileges to connect to your cloud data warehouse. The warehouse must contain the data ThoughtSpot will use to create Answers, Liveboards, and Worksheets.
- **Unique Connection Name**: Each new SpotApp connection name must be unique.
- **Administrator Access to Google Ads**: Maintain administrator access to manage Google Ads.
- **Access to Google Ads Tables**: Ensure access to the following Google Ads tables in your cloud data warehouse:
  - `GOOGLEADS_AD`
  - `GOOGLEADS_CAMPAIGN`
  - `GOOGLEADS_KEYWORD`
  - `GOOGLEADS_GEO`

Refer to the Google Ad Analysis SpotApp schema for more details on the data structure and requirements.


## Deploy the SpotApp

After you have downloaded the Zip file and verified its contents, follow these steps:

1. Log into your ThoughtSpot instance and create an Embrace connection to all of the relevant views.
2. Import the TML for the worksheets and verify that it has all been imported without any errors.
3. Import the TML for the pinboard and verify that it has all been imported without any errors.
4. You are ready to start searching your Databricks data!

For detailed instructions on how to import TML files, refer to the [ThoughtSpot documentation](https://docs.thoughtspot.com/software/latest/tml-import-export-multiple).
