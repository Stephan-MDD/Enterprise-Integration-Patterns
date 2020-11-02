  
  
  
  
  
#  Assignment 7 | Enterprise Integration Patterns
  
  
_System Integration, fall 2020_
  
Author  
**Stephan Djurhuus**
  
![cover image](/assets/cover.png?0.33382428783723506 )  
  
##  Content
  
  
- [Objectives](/#objectives )
- [Essential System Integration Glossary](/#essential-system-integration-glossary )
  - [Basic Messaging Concepts](/#basic-messaging-concepts )
    - [Channels](/#channels )
    - [Messages](/#messages )
    - [Pipes and Filters](/#pipes-and-filters )
    - [Routing](/#routing )
    - [Transformation](/#transformation )
    - [Endpoints](/#endpoints )
  - [Message Channel](/#message-channel )
    - [Channels](/#channels-1 )
    - [Message Channel Application Names](/#message-channel-application-names )
    - [Channel Types](/#channel-types )
  - [Pipes & Filters](/#pipes-filters )
    - [Pipe](/#pipe )
    - [Filter](/#filter )
    - [Pipeline Processing](/#pipeline-processing )
    - [Parallel Processing](/#parallel-processing )
  
##  Objectives
  
  
Message-Oriented Middleware is among the most popular technologies used for connecting
applications. The best practices in implementing messaging systems in enterprise application
integration refer to applying enterprise integration patterns (EIP).
  
Your task is to read [Chapter 3: Messaging Systems](https://www.enterpriseintegrationpatterns.com/docs/EnterpriseIntegrationPatterns_HohpeWoolf_ch03.pdf ) and create a glossary of at least ten terms, related to System Integration, which you find essential.
  
[Extended Description](https://datsoftlyngby.github.io/soft2020fall/resources/0dc4c4f6-A7-EIP.pdf )
  
##  Essential System Integration Glossary
  
  
  
###  Basic Messaging Concepts
  
  
####  Channels
  
  
A virtual pipe that connects a sender to a receiver.
  
####  Messages
  
  
An atomic packet of data that can be transmitted on a channel.
  
####  Pipes and Filters
  
  
Describes how multiple processing steps can be
chained together using channels.
  
####  Routing
  
  
Determines how to navigate the channel topology and directs the message to the final receiver, or at least to the next router.
  
####  Transformation
  
  
A Message Translator, which converts the message from one format to another.
  
####  Endpoints
  
  
A set of coordinated Message Endpoints that enable the application to send and receive messages.
  
  
###  Message Channel
  
  
> "When an application has information to communicate, it doesn’t just fling the information into the messaging system but adds the information to a particular Message Channel. An application receiving information doesn’t just pick it up at random from the messaging system; it retrieves the information from a particular Message Channel."
  
####  Channels
  
  
Logical addresses in the messaging system.  
How they’re actually implemented depends on the messaging system product and its implementation.
  
Examples:
  
-   Message Endpoint has a direct connection to every other endpoint.
-   They’re all connected through a central hub.
-   Several separate logical channels are configured as one physical channel.
  
####  Message Channel Application Names
  
  
-   Sender and Receiver
-   Producer and Consumer
-   Publisher and Subscriber
-   Requester and Provider
  
> "When dealing with Web services, the application that sends a message to the service provider is often referred to as the consumer of the service even though it sends the request message. We can think of it in such a way that the consumer sends a message to the provider and then consumes the response."
  
####  Channel Types
  
  
-   Point-to-Point Channels
-   Publish-Subscribe Channels
  
  
###  Pipes & Filters
  
  
![](/assets/pipes-filters.png?0.7473056547552726 )  
  
> The Pipes and Filters style uses abstract pipes to decouple components from each other. The pipe allows one component to send a message into the pipe so that it can be consumed later by another process that is unknown to the component... <br><br>This affords us the flexibility to move a processing step to a different machine for dependency, maintenance, or performance reasons.
  
####  Pipe
  
  
Messaging channels
  
####  Filter
  
  
Individual processing steps.
  
Examples:
  
-   Decrypt encrypted message.
-   Authenticate content
-   Avoid duplicates
  
####  Pipeline Processing
  
  
For example, after the first message has been decrypted, it can be passed on to the authentication component. At the same time, the next message can already be decrypted.
  
![](/assets/processing-pipeline.png?0.2970307647204762 )  
  
####  Parallel Processing
  
  
In this scenario, a Point-to-Point Channel with Competing Consumers is needed to guarantee that each message on the channel is consumed by exactly one of N available processors.
  
![](/assets/parallel-processing.png?0.36144598562277785 )  
  
  
---
  
Software Development @ Copenhagen Business Academy, Denmark 2020
  