# Scan and Query API

    # Dynamodb Scan API:
        1 The scan operation return one or more item and it attribute by accessing every time in table
        2 To have DynamoDB return fewer item , you can provide filter expression
        3 Scan API can use a lot of RCU as they access every item in table
        4 Scan operation operate in sequence 
        5 Scan can use eventually consistence read when access the data in table
        6 if you need consistent copy of data , scan the item of scan begin, You can set `consistentRead` parameter to `true`
        7 If the total number of scanned items exceeds the maximum dataset size limit of 1 MB, the scan stops and results are returned to the user as a LastEvaluatedKey value to continue the scan in a subsequent operation. T

        # DynamoDB scan API with projection API
            1 ) in this example scan will return all post in the forum that were posted within date range and have more than 50 replicas
             