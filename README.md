### Understanding publisher and message broker
1. How many data your publisher program will send to the message broker in one run? <br>
    It will send 5 data, each `publish_event` call sends one message.
2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? <br>
   The URL `amqp://guest:guest@localhost:5672` is the same in both the publisher and subscriber programs because it 
specifies the location of the AMQP broker and the credentials needed to connect to it. In this case, it indicates that 
the broker is running on the local machine (localhost) and is accessible using the default guest credentials (username: 
guest, password: guest).

### Running RabbitMQ as message broker
![img.png](img.png)

### Sending and processing event.
![img_1.png](img_1.png)

### Monitoring chart based on publisher.
![img_2.png](img_2.png) <br>
The spikes in the RabbitMQ browser charts are likely related to the publisher sending messages. Each spike 
corresponds to the moment when the publisher sends a batch of messages. As the publisher sends messages, RabbitMQ 
processes them and adds them to the queues. This processing and queuing of messages can cause spikes in the charts, indicating increased activity on the message broker.