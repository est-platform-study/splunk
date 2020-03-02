# getting data in
- only admin user can ingest data to index
- three options to ingest data
    - upload
        - get data from file of user's computer
        - it creates index once    
    - monitor
        - it is for monitoring files, http event, tcp/udp or scripts
        - list of monitoring target
        ```
        - event logs
        - file system changes
        - active directoy
        - network information
        ```
    - forward
        - it can receive data from external forwarder
        - probably it would be main source of data input in production environment
## upload process
- it can recognize how file data is formatted and make source type automatically
- if source type is incorrect, we can make our source type
- predefine source type can divide target file to index to splunk
- hostname means where this data comes from
## why divide index
- it can make search fast
- admin can limit what user can see through limit index
- separate indexes allow custom retention policies

## monitoring
- difference between monitoring and monitoring is that monitoring keeps watching target file
- if directory is selected to be monitored, it can make white list and black list
