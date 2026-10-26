# Experiment 4: Mutual Exclusion Using Semaphore and Mutex

## Aim
To implement Mutual Exclusion using semaphore and monitor.

## Part A – Mutual Exclusion Using Semaphore

### Description
This program demonstrates mutual exclusion using a semaphore. Multiple customer threads withdraw money from a shared ATM balance. The semaphore ensures that only one thread accesses and modifies the shared balance at a time, preventing race conditions.

### Program Details
- **Initial Balance:** 1000
- **Withdrawal Amount:** 100 per customer
- **Synchronization:** Semaphore
- **Header Files:** `stdio.h`, `pthread.h`, `semaphore.h`

### Compile and Run
```bash
gcc experiment4_semaphore.c -o semaphore -pthread
./semaphore
```

### Sample Output
The program asks for the number of customers and displays the updated balance after each withdrawal.

Example:
```text
Enter customers: 3
Customer 1: Balance=900
Customer 3: Balance=800
Customer 2: Balance=700
```

### Output Screenshot
![Semaphore Output](experiment4_semaphore_output.png)

---

## Part B – Mutual Exclusion Using Mutex

### Description
This program demonstrates mutual exclusion using a mutex. Multiple vehicle threads access a shared parking slot count. The mutex ensures that only one thread updates the number of available slots at a time.

### Program Details
- **Initial Parking Slots:** 5
- **Operation:** Each vehicle occupies one parking slot.
- **Synchronization:** Mutex
- **Header Files:** `stdio.h`, `pthread.h`

### Compile and Run
```bash
gcc experiment4_mutex.c -o mutex -pthread
./mutex
```

### Sample Output
The program asks for the number of vehicles and displays the remaining parking slots after each vehicle parks.

Example:
```text
Enter vehicles: 3
Vehicle 1: Slots=4
Vehicle 2: Slots=3
Vehicle 3: Slots=2
```

### Output Screenshot
![Mutex Output](experiment4_mutex_output.png)

---

## Concepts Used
- Mutual Exclusion
- Semaphore
- Mutex
- Threads
- Critical Section
- Race Condition
- Process Synchronization

## Result
Mutual exclusion using semaphore and mutex is demonstrated by controlling concurrent access to shared resources and preventing race conditions.
