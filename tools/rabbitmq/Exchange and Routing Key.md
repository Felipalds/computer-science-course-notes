## What is it?
A routing key is a string that the producer sends in the header of the request. Is tells the exchange how to manage the new message (to which queues it should be).

```
@Bean  
public Exchange orderExchange () {  
    return ExchangeBuilder.directExchange("orderExchange").durable(true).build();  
}  
  
@Bean  
public Queue orderNotificationAdminQueue () {  
    return QueueBuilder.durable("orderNotificationAdminQueue").build();  
}  
  
@Bean  
public Binding orderBinding (Queue orderNotificationAdminQueue, Exchange orderExchange) {  
    return BindingBuilder.bind(orderNotificationAdminQueue).to(orderExchange).with("orderRoutingKey").noargs();  
}

```
