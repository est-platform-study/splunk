# main topic
- Introduction to Splunk's interface
- Basic searching
- Using fields in searches
- Search fundamentals
- Transforming commands
- Creating reports and dashboards
- Creating and using lookups
- Scheduled reports
- Alerts
- Using Pivot


# sub topic
## 1 Splunk Basics 
1. Splunk components
    - purpose of splunk
        - index data
        - search & investigate
        - add knowledge
        - monitor & alert
        - report & analyze 
    - three components
        - indexer
        - search head
            - search heads also provide tools to enhance the search experience such as reports, dashboards and visualizations
        - forwarder
    - additional splunk components
        - deployment server
        - cluster master
        - license master
2. Understand the uses of Splunk
    - standalone
        - all functions in a single instance of splunk
        - for testing, proof of concept, personal use, and learning
    - basic
        -basic deployment for organizations
            - indexing less than 20GB per day
            - with under 20 users
            - small amount of forwarders
        - splunk server
            - similar to standalone
            - manage deployment of forwarder configurations
        - forwarders
    - multi-instance
        - deployment for organizations
            - indexing up to 100GB per day
            - supports 100 users
            - suports several hundred forwarders
    - index cluster
        - traditional index cluster
            - configured to replicate data
            - prevent data loss
            - promote availability
            - manage multiple indexers
        - non-replicating index clusters
            - offer simplified management
            - do not provide availability or data recovery            
3. Define Splunk apps
    - default apps are home app, search and report
    ### home app
    - home app is default app
    - customer can select default app
    ### search & reporting app
    - provides a default interface for searching and analyzing data
    - enables to create knowledge objects, reports, and dashboards
    - data summary tabs
        - host
            - unique identifier of where the event originated
        - source
            - name of the file, stream, or other input
        - sourcetype
            - specific data type or data format 
    - event tab
        - selected fields
            - host, source, sourcetype   
4. Customizing user settings
    - Set time zone
    - Adjust the contrast for better accessibility
    - Change your password
5. Basic navigation in Splunk

## 2 Basic Searching 
1. Run basic searches
2. Set the time range of a search
3. Identify the contents of search results
4. Refine searches
5. Use the timeline
6. Work with events
7. Control a search job
8. Save search results

## 3 Using Fields in Searches 
1. Understand fields
2. Use fields in searches
3. Use the fields sidebar

## 4 Search Language Fundamentals 
1. Review basic search commands and general search practices
2. Examine the search pipeline
3. Specify indexes in searches
4. Use the following commands to perform searches: tables, rename, fields, dedup, & sort

## 5 Using Basic Transforming Commands 
1. The top command
2. The rare command
3. The stats command

## 6 Creating Reports and Dashboards
1. Save a search as a report
2. Edit reports
3. Create reports that display statistics (tables)
4. Create reports that display visualizations (charts)
5. Create a dashboard
6. Add a report to a dashboard
7. Edit a dashboard

## 7 Creating and Using Lookups 
1. Describe lookups
2. Examine a lookup file example
3. Create a lookup file and create a lookup definition
4. Configure an automatic lookup
5. Use the lookup in searches

## 8 Creating Scheduled Reports and Alerts 
1. Describe scheduled reports
2. Configure scheduled reports
3. Describe alerts
4. Create alerts
5. View fired alerts