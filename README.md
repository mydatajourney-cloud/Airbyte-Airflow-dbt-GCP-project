# Airbyte-Airflow-dbt-GCP Projects

## Airbyte Overview
Airbyte is an open-source data integration platform that helps you sync data between various sources and destinations.

### Source
The **Source** feature in Airbyte is responsible for connecting and extracting data from various sources like databases, web services, or applications. The source handles:
- Establishing the connection
- Query configuration
- Synchronizing data to provide it to the integration system.

---

## How to Set Up a MySQL Source in Airbyte

### Step 1: Create a New Source
1. On the Airbyte main page, click on **Sources** from the navigation menu.
2. Click on **+ New Source** or **Add Source**.

![Airbyte Add Source](https://github.com/user-attachments/assets/0e6b156d-8acc-4a65-9cd0-07b627eac8a4)

### Step 2: Select MySQL as the Data Source
1. From the list of available data sources, select **MySQL**.

![MySQL Selection](https://github.com/user-attachments/assets/21a71df1-3646-4b99-9bc8-1a455ea98b2f)

### Step 3: Provide Connection Information
1. Fill in the required details in the MySQL source configuration form:
   - **Host**: IP address or domain name of the MySQL server.
   - **Port**: The port where MySQL is listening (default is 3306).
   - **Database**: The name of the database you want to connect to.
   - **Username**: Username to access the MySQL database.
   - **Password**: Password for the corresponding username.
   - **Additional Parameters (Optional)**: Provide any additional parameters like SSL encryption if needed.

### Step 4: Save the Configuration
1. If the connection is successful, click on **Set up source** or **Save** to save the source configuration.

---

## Destination
The **Destination** feature in Airbyte handles receiving and storing the extracted data from the source into storage systems or databases like BigQuery, Snowflake, or Amazon Redshift. It allows configuration options such as:
- Specifying datasets
- Structuring tables
- Configuring sync methods

---

## How to Set Up a BigQuery Destination in Airbyte

### Step 1: Access Airbyte
1. Open your browser and log in to the Airbyte interface.

![Airbyte UI](https://github.com/user-attachments/assets/db635b4e-1bb8-4fc5-9b77-8a7b36523f5e)

### Step 2: Create a New Destination
1. From the Airbyte main page, click on **Destinations** from the navigation menu.
2. Click on **+ New Destination** or **Add Destination**.
3. From the list of destinations, select **BigQuery**.

![BigQuery Selection](https://github.com/user-attachments/assets/909ac9dc-74b7-46ba-a229-eec305957359)

### Step 3: Provide BigQuery Configuration Information
1. Fill in the required details for the BigQuery destination:
   - **Project ID**: The Google Cloud project ID where BigQuery is set up.
   - **Dataset**: The name of the dataset you want to store the data in.
   - **JSON Key File**: Upload the JSON file that contains the service account credentials for accessing BigQuery. (You can generate this file from the Google Cloud Console).

![BigQuery Config](https://github.com/user-attachments/assets/379ead50-1407-41d2-b548-5b26b530ed5c)

### Step 4: Save the Configuration
1. Once the connection is successful, click on **Set up destination** or **Save**.

---

## Connection
A **Connection** is a configuration link between a **Source** and a **Destination**, allowing data transfer and synchronization between them. It lets you:
- Configure sync modes (e.g., full refresh, incremental sync)
- Set sync frequency and primary keys
- Manage how data flows between systems

---

## How to Set Up a Connection in Airbyte

### Step 1: Access Airbyte
1. Open your browser and log in to the Airbyte interface.

![Airbyte UI](https://github.com/user-attachments/assets/0180224c-5588-46d5-bcb7-f6eef484e49b)

### Step 2: Create a New Connection
1. From the Airbyte main page, click on **Connections** in the navigation menu.
2. Click on **+ New Connection** or **Add Connection**.

### Step 3: Select Source and Destination
1. In the Connection setup, select the **Source** and **Destination** from the pre-configured list:
   - **Source**: Choose the previously configured MySQL source.
   
   ![Source Selection](https://github.com/user-attachments/assets/80a08b17-5aa1-40ac-a885-95a330ac64ad)

   - **Destination**: Choose the previously configured BigQuery destination.

   ![Destination Selection](https://github.com/user-attachments/assets/2ee404a1-76fb-4319-929a-264008ea2e3f)

### Step 4: Configure Data Sync
1. **Sync Mode**: Choose the sync mode:
   - **Append Historical Changes**
   - **Append New Rows and Updates Only**

   ![Sync Mode](https://github.com/user-attachments/assets/1147879c-36ea-4fa4-92cb-5c24d168267f)

2. **Field Mapping**: Select the schema and tables you want to sync to BigQuery, then click **Sync**.

   ![Field Mapping](https://github.com/user-attachments/assets/6c3963c1-f051-441f-8470-23804e30076b)

### Step 5: Preview and Test the Connection
1. **Sync Frequency**: Choose the sync frequency (e.g., daily, hourly, or manual sync).

   ![Sync Frequency](https://github.com/user-attachments/assets/4bc29415-02d6-4d04-bbc1-97a4fd90afe7)

2. **Test Connection**: (Optional) Test the connection to ensure data can be synced successfully.

### Step 6: Save and Activate Connection
1. Click **Save** or **Create Connection** to store the configuration.
2. **Start Sync**: The sync will automatically start based on the set frequency. You can also manually trigger the sync by clicking **Manual Sync**.

---

This setup guide will help you configure Airbyte's Source, Destination, and Connection settings for a seamless data integration process.
