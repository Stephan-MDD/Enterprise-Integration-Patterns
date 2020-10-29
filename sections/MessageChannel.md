### Message Channel

> "When an application has information to communicate, it doesn’t just fling the information into the messaging system but adds the information to a particular Message Channel. An application receiving information doesn’t just pick it up at random from the messaging system; it retrieves the information from a particular Message Channel."

#### Channels

Logical addresses in the messaging system.

How they’re actually implemented depends on the messaging system product and its implementation.

Examples:

-   Message Endpoint has a direct connection to every other endpoint.
-   They’re all connected through a central hub.
-   Several separate logical channels are configured as one physical channel.

#### Message Channel Application Names

-   Sender and Receiver
-   Producer and Consumer
-   Publisher and Subscriber
-   Requester and Provider

> When dealing with Web services, the application that sends a message to the service provider is often referred to as the consumer of the service even though it sends the request message. We can think of it in such a way that the consumer sends a message to the provider and then consumes the response.

#### Channel Types

-   Point-to-Point Channels
-   Publish-Subscribe Channels
