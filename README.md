# ativ-circuitbreaker

Circuit Breaker implemented using Resilence4J. The page "/albums" (not the index page) runs a connection with a generic JSON API. Should the API fail to respond, the system will throw (See: Throwable) a default return for the request as an error response. Should it fail enough times, namely around 50 times (As defined by the circuitbreaker config "circuitBreaker", in line 39 of DemoApplication), it will shift the state of the circuit to open for 1000 miliseconds (waitDurationInOpenState), then switch to half-open
