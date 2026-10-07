# EC2-Life-Cycle

EC2 Life Cycle ka matlab hai EC2 instance ki different states, jo instance ke start hone se lekar stop ya terminate hone tak hoti hain.

## 1. Pending

EC2 instance start ho raha hota hai aur AWS required resources prepare karta hai.

**Easy Meaning:** Instance start hone ki process mein hai.

## 2. Running

Instance successfully start ho jata hai aur hum is par applications aur services run kar sakte hain.

**Easy Meaning:** EC2 properly chal raha hai.

## 3. Stopping

Running instance ko stop kiya ja raha hota hai.

**Easy Meaning:** Instance band hone ki process mein hai.

## 4. Stopped

Instance temporarily band hota hai, lekin baad mein dobara start kiya ja sakta hai.

**Easy Meaning:** EC2 filhaal off hai.

## 5. Starting

Stopped instance ko dobara start kiya ja raha hota hai.

**Easy Meaning:** EC2 dobara on ho raha hai.

## 6. Shutting-down

Instance ko permanently terminate karne ki process start ho jati hai.

**Easy Meaning:** EC2 permanently delete hone ki process mein hai.

## 7. Terminated

Instance permanently terminate ho jata hai aur normally dobara start nahi kiya ja sakta.

**Easy Meaning:** EC2 permanently delete ho gaya.

## Life Cycle Flow

**Pending → Running → Stopping → Stopped → Starting → Running**

For permanent termination:

**Running → Shutting-down → Terminated**

### Quick Revision

| State         | Meaning                |
| ------------- | ---------------------- |
| Pending       | Starting               |
| Running       | Working                |
| Stopping      | Being stopped          |
| Stopped       | Temporarily off        |
| Starting      | Starting again         |
| Shutting-down | Being terminated       |
| Terminated    | Permanently terminated |

**Conclusion:**
EC2 Life Cycle humein samajhne mein help karta hai ke EC2 instance kis state mein hai aur usay kab start, stop ya terminate kiya ja sakta hai.
# EC2 Life Cycle

```text
                 ┌─────────────┐
                 │   PENDING   │
                 │  Starting   │
                 └──────┬──────┘
                        ↓
                 ┌─────────────┐
                 │   RUNNING   │
                 │   Working   │
                 └──────┬──────┘
                        ↓
                 ┌─────────────┐
                 │  STOPPING   │
                 │ Being Stop  │
                 └──────┬──────┘
                        ↓
                 ┌─────────────┐
                 │   STOPPED   │
                 │ Temporarily │
                 │     Off     │
                 └──────┬──────┘
                        │
                        │ Start Again
                        ↓
                 ┌─────────────┐
                 │  STARTING   │
                 │  Starting   │
                 │    Again    │
                 └──────┬──────┘
                        ↓
                    RUNNING
```

### Permanent Termination

```text
RUNNING
   ↓
SHUTTING-DOWN
   ↓
TERMINATED
```

**Easy Flow:**
**Pending → Running → Stopping → Stopped → Starting → Running**

**Permanent Delete:**
**Running → Shutting-down → Terminated**





