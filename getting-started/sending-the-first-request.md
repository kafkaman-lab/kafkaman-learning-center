# Sending the first request

<br />

kafkaman makes it easy to interact with Kafka and Schema Registry. Consume data, produce new data from a data source, admin your cluster. You don't need to enter commands in a terminal or write any code. Create a new request and select **Send**, and the response appears right inside kafkaman.

## Kafka requests defined

Kafka is a distributed system consisting of servers and clients that communicate via a high-performance <a href="https://kafka.apache.org/protocol.html">TCP network protocol</a>.

A request includes :

*  `Kafka Cluster connection` The kafka <a href="/docs/connections/">connection</a> used to connect
*  `Schema Registry connection` The kafka <a href="/docs/connections/">connection</a> used to connect
*  `Method` The method indicates the action you want to perform
*  `Topic` The topic to be used
*  `Key` The message key to be send or used to filter consumed data
*  `Event` The message event to be send or used to filter consumed data

## Sending a request

Ready to send your first request? Open kafkaman and try the following:

1. Select the **+** button (near the top of kafkaman) to open a new tab.
2. Select the connections for the request.
3. Select the consume method.
4. Select the topic.
5. Click  **Run** or **Start**.

You will see the response data sent from the cluster in the lower pane.

<img alt="Sending a request" src="https://raw.githubusercontent.com/kafkaman-lab/kafkaman-learning-center/main/assets/firstRequestSend.png" width="716px">

### What just happened?

In this example, kafkaman is acting as the client application and is communicating with an Kafka server. Here's what happened when you selected **Run** or **Start**:

1. kafkaman create a connection with Kafka cluster and start a consumer with the specified parameters.
1. The Kafka broker received the request, processed it, and returned a response to kafkaman.
1. kafkaman received the response and displayed it in the **Response** pane.

You have just used kafkaman to create a consumption group in a Kafka cluster and retrieve existing records on the selected topic. It's okay to take a moment to sit back and reflect on how great it is!

<br />

## Next steps

When you're ready, learn more about [building and sending requests in kafkaman](/docs/sending-requests/requests/).
