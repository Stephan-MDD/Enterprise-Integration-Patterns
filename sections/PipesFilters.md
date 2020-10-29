### Pipes & Filters

@import "/assets/pipes-filters.png"

> The Pipes and Filters style uses abstract pipes to decouple components from each other. The pipe allows one component to send a message into the pipe so that it can be consumed later by another process that is unknown to the component... <br><br>This affords us the flexibility to move a processing step to a different machine for dependency, maintenance, or performance reasons.

#### Pipe

Messaging channels

#### Filter

Individual processing steps.

Examples:

-   Decrypt encrypted message.
-   Authenticate content
-   Avoid duplicates

#### Pipeline Processing

For example, after the first message has been decrypted, it can be passed on to the authentication component. At the same time, the next message can already be decrypted.

@import "/assets/processing-pipeline.png"

#### Parallel Processing

In this scenario, a Point-to-Point Channel with Competing Consumers is needed to guarantee that each message on the channel is consumed by exactly one of N available processors.

@import "/assets/parallel-processing.png"
