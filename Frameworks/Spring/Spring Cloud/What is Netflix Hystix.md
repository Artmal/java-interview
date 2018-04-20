## What is Hystrix?
Netflix Hystrix is the implementation of Circuit Breaker pattern. The main idea is that request goes to circuit breaker and if it's sees that the supplier fails it's prevent all subsequent loads and prevents resources leakage and cascade failure of components. You can define method which will be executed if such things happened and give time to a component to recover.
