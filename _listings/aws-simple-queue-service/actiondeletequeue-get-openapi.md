---
swagger: "2.0"
x-collection-name: AWS Simple Queue Service
x-complete: 0
info:
  title: AWS Simple Queue Service API Delete Queue
  version: 1.0.0
  description: Deletes the queue specified by the QueueUrl, even if the queue is empty.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateQueue:
    get:
      summary: Create Queue
      description: Creates a new standard or FIFO queue or returns the URL of an existing
        queue.
      operationId: createQueue
      x-api-path-slug: actioncreatequeue-get
      parameters:
      - in: query
        name: |-
          Attribute
                      , Attribute.N.Name (key), Attribute.N.Value (value)
        description: A map of attributes with their corresponding values
        type: string
      - in: query
        name: QueueName
        description: The name of the new queue
        type: string
      responses:
        200:
          description: OK
      tags:
      - Queues
  /?Action=DeleteQueue:
    get:
      summary: Delete Queue
      description: Deletes the queue specified by the QueueUrl, even if the queue
        is empty.
      operationId: deleteQueue
      x-api-path-slug: actiondeletequeue-get
      parameters:
      - in: query
        name: QueueUrl
        description: The URL of the Amazon SQS queue to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Queues
  /?Action=GetQueueAttributes:
    get:
      summary: Get Queue Attributes
      description: Gets attributes for the specified queue.
      operationId: getQueueAttributes
      x-api-path-slug: actiongetqueueattributes-get
      parameters:
      - in: query
        name: AttributeName.N
        description: A list of attributes for which to retrieve information
        type: string
      - in: query
        name: QueueUrl
        description: The URL of the Amazon SQS queue whose attribute information is
          retrieved
        type: string
      responses:
        200:
          description: OK
      tags:
      - Queues
  /?Action=GetQueueUrl:
    get:
      summary: Get Queue Url
      description: Returns the URL of an existing queue.
      operationId: getQueueUrl
      x-api-path-slug: actiongetqueueurl-get
      parameters:
      - in: query
        name: QueueName
        description: The name of the queue whose URL must be fetched
        type: string
      - in: query
        name: QueueOwnerAWSAccountId
        description: The AWS account ID of the account that created the queue
        type: string
      responses:
        200:
          description: OK
      tags:
      - Queues
  /?Action=ListDeadLetterSourceQueues:
    get:
      summary: List Dead Letter Source Queues
      description: Returns a list of your queues that have the RedrivePolicy queue
        attribute configured with a dead letter queue.
      operationId: listDeadLetterSourceQueues
      x-api-path-slug: actionlistdeadlettersourcequeues-get
      parameters:
      - in: query
        name: QueueUrl
        description: The URL of a dead letter queue
        type: string
      responses:
        200:
          description: OK
      tags:
      - Queues
  /?Action=ListQueues:
    get:
      summary: List Queues
      description: Returns a list of your queues.
      operationId: listQueues
      x-api-path-slug: actionlistqueues-get
      parameters:
      - in: query
        name: QueueNamePrefix
        description: A string to use for filtering the list results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Queues
  /?Action=PurgeQueue:
    get:
      summary: Purge Queue
      description: Deletes the messages in a queue specified by the QueueURL parameter.
      operationId: purgeQueue
      x-api-path-slug: actionpurgequeue-get
      parameters:
      - in: query
        name: QueueUrl
        description: The URL of the queue from which the PurgeQueue action deletes
          messages
        type: string
      responses:
        200:
          description: OK
      tags:
      - Queues
  /?Action=SetQueueAttributes:
    get:
      summary: Set Queue Attributes
      description: Sets the value of one or more queue attributes.
      operationId: setQueueAttributes
      x-api-path-slug: actionsetqueueattributes-get
      parameters:
      - in: query
        name: |-
          Attribute
                      , Attribute.N.Name (key), Attribute.N.Value (value)
        description: A map of attributes to set
        type: string
      - in: query
        name: QueueUrl
        description: The URL of the Amazon SQS queue whose attributes are set
        type: string
      responses:
        200:
          description: OK
      tags:
      - Queues
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---