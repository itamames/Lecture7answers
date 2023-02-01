# Lecture7answers

1.
```java
	if (customerArrives(ARRIVAL_PROBABILITY))
		q.add(new Customer(minute));

	for (int i = 0; i < NUM_REGISTERS; i++) {
		if (registerAvailableTimes[i] <= minute && !q.isEmpty()) {
			Customer customer = q.remove();
			numCustomers++;
			totalWaitTime += minute - customer.getTimeEnteredQueue();
			registerAvailableTimes[i] = 
				minute + customer.getTimeNeededAtRegister();
		}
	}
```
2.
```java
	if (customerArrives(ARRIVAL_PROBABILITY))
		emptiestQueue(queues).add(new Customer(minute));
	for (int i = 0; i < NUM_REGISTERS; i++)
		if (registerAvailableTimes[i] <= minute && !queues[i].isEmpty()) {
			Customer customer = queues[i].remove();
			numCustomers++;
			totalWaitTime += minute - customer.getTimeEnteredQueue();
			registerAvailableTimes[i] = 
				minute + customer.getTimeNeededAtRegister();
		}
	}
```
