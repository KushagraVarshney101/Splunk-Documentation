# Sample Usage: Searching Web Server Logs in Splunk and Adding to Dashboard

## Introduction

In this guide, we will walk through the steps of creating a sample web server log, searching for it in Splunk, and adding the search results to a dashboard for easy access. We will also provide a reference video to show how to complete each step.

### Prerequisites:
- Splunk is installed and running on your system.
- A Splunk instance is set up to index data.

## Step 1: Create a Sample Web Server Log

To simulate web server logs, we'll create a simple log file that mimics entries from a web server, including details like IP address, timestamp, request method, URL, status code, and response time.

### Sample Web Server Log Format:


Save the log data to a file called `sample_web_server.log` or download it from here [Web Logs](https://github.com/KushagraVarshney101/Splunk-Documentation/blob/main/Sample%20Logs/webserver.log).

## Step 2: Upload the Log File to Splunk

1. Log in to your Splunk instance.
2. Go to **Settings > Add Data**.
3. Select **Upload** under the "Local File" option.
4. Browse to the location of the `sample_web_server.log` file and upload it.
5. Choose the appropriate source type (you can use `access_combined` for web server logs or create a custom source type).
6. Click **Next** and then **Review** and **Submit** to complete the upload process.

Splunk will now index your log file and make it available for searching.

## Step 3: Search for the Log Data in Splunk

Once the log data is indexed, you can perform a search to query the logs.

### Example Search Query:

1. Go to the **Search & Reporting** app in Splunk.
2. In the search bar, enter the sample query(b) [sample queries](https://github.com/KushagraVarshney101/Splunk-Documentation/blob/main/Sample%20Queries/Search%20queries.md) to filter the logs and display the relevant fields and change the hostname to your one:
     
This query will display the following columns:
- `_time`: The timestamp of the request.
- `clientip`: The IP address of the client.
- `method`: The HTTP request method (GET, POST, etc.).
- `uri`: The requested URI.
- `status`: The HTTP status code.
- `bytes`: The response size.

3. Hit **Enter** to execute the query and review the search results. You should see your web server logs displayed in a table format.

## Step 4: Add the Search to a Dashboard

1. After running the search query, click the **Save As** button above the search results.
2. Select **Dashboard Panel** from the dropdown menu.
3. In the **Create Dashboard Panel** window:
- Choose an existing dashboard or create a new one (e.g., "Web Server Logs").
- Give the panel a title, such as "Web Server Logs Overview".
4. Click **Save** to add the search results as a panel to your dashboard.

Now, the web server log search results will be part of your dashboard, making it easier to access and visualize the logs.

## Step 5: Screen Capture

For reference, I have recorded a screen capture that walks through the steps outlined in this document. The video will show:

- How to create and upload the sample web server log.
- How to perform the search query in Splunk.
- How to add the search results to a dashboard.

You can view the recorded video [here](insert-link-to-video).

## Conclusion

You have now successfully uploaded a sample web server log to Splunk, searched for the data using a Splunk query, and added the results to a dashboard for better visualization. Refer to the video tutorial for additional guidance.

If you have any questions or run into issues, feel free to reach out to the support team or consult the official Splunk documentation.
