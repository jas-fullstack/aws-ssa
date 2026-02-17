# EC2
## EC2 instance types
## 📌 EC2 Instance Family Reference

| Letter | Official Category Name        | What It Represents                     |
|--------|------------------------------|----------------------------------------|
| T      | Burstable Performance         | Low baseline CPU + CPU credits         |
| M      | General Purpose               | Balanced CPU & Memory                  |
| C      | Compute Optimized             | High CPU                               |
| R      | Memory Optimized              | High RAM                               |
| I      | Storage Optimized             | High IOPS / NVMe                       |
| P      | Accelerated Computing         | GPU (ML training)                      |
| G      | Accelerated Computing         | GPU (graphics / inference)             |
| D      | Dense Storage                 | Large HDD storage                      |
| X      | Memory Optimized (Extreme)    | Very large RAM                         |
| H      | Storage Optimized             | High disk throughput                   |

---

## 🧠 How to Choose the Correct Instance (Exam Strategy)

### Step 1: Identify the Bottleneck

- High CPU usage → Choose **C**
- Out of Memory errors → Choose **R**
- High disk latency / IOPS required → Choose **I**
- Mostly idle with occasional spikes → Choose **T**
- Balanced normal application → Choose **M**

- # 🖥️ AWS EC2 Instance Families with Examples

---

## 🧮 CPU Related

| Letter | Category | What It Means | Example Instance Types |
|--------|----------|---------------|------------------------|
| C | Compute Optimized | High CPU performance | c6i, c7g, c5 |
| T | Burstable Performance | CPU credits (spiky workloads) | t3, t3a, t4g |

---

## 🧠 Memory Related

| Letter | Category | What It Means | Example Instance Types |
|--------|----------|---------------|------------------------|
| R | Memory Optimized | High RAM | r6i, r7g, r5 |
| X | Memory Optimized (Extreme) | Very large RAM | x2idn, x1e |

---

## 💾 Storage Related

| Letter | Category | What It Means | Example Instance Types |
|--------|----------|---------------|------------------------|
| I | Storage Optimized | High IOPS (NVMe SSD) | i3, i4i |
| D | Dense Storage | Large HDD storage | d3, d2 |
| H | Storage Optimized | High disk throughput | h1 |

---

## ⚖️ Balanced

| Letter | Category | What It Means | Example Instance Types |
|--------|----------|---------------|------------------------|
| M | General Purpose | Balanced CPU & Memory | m6i, m7g, m5 |

---

## 🎮 GPU / Accelerated

| Letter | Category | What It Means | Example Instance Types |
|--------|----------|---------------|------------------------|
| P | Accelerated Computing | ML training (GPU) | p4, p5 |
| G | Accelerated Computing | Graphics / ML inference | g5, g4dn |

---


---

## 🔥 Quick Decision Rule (Memorize This)


# 🛒 EC2 Purchasing Options (AWS)

AWS EC2 offers multiple ways to buy compute capacity depending on cost, availability, and workload characteristics.

---

## 🟢 1. **On-Demand Instances**
**What it is:**  
Pay for compute by the second, with no long-term commitment.

**Best for:**  
- Development / testing  
- Unpredictable workloads  
- Short-lived applications

**Pros:**  
✔ No upfront cost  
✔ Flexible scaling

**Cons:**  
✖ Highest cost per hour

---

## 🔒 2. **Reserved Instances (RI)**
**What it is:**  
Commit to a 1- or 3-year term in exchange for a big discount.

**Best for:**  
- Steady state production workloads  
- Long-term predictable usage

**Types:**
- Standard RI – max discount
- Convertible RI – change instance types
- Scheduled RI – specific time slots

**Pros:**  
✔ Lower cost than On-Demand  

**Cons:**  
✖ Requires commitment

---

## 💰 3. **Savings Plans**
**What it is:**  
Commit to a consistent $/hr spend for 1 or 3 years.

**Best for:**  
- Predictable cost savings across EC2 usage  
- Want flexibility across instance types

**Types:**
- Compute Savings Plans – most flexible
- EC2 Instance Savings Plans – specific instance family

**Pros:**  
✔ Big discounts like RI  
✔ More flexible than Reserved Instances

---

## 💥 4. **Spot Instances**
**What it is:**  
Buy unused EC2 capacity at steep discounts (up to ~90% off).

**Best for:**  
- Fault-tolerant, interruptible workloads  
- Batch jobs, big data, CI/CD

**Behavior:**
- AWS can reclaim Spot instances with a 2-minute warning

**Pros:**  
✔ Lowest cost

**Cons:**  
✖ Not suitable for critical apps

---

## 🧱 5. **Dedicated Hosts**
**What it is:**  
Physical server dedicated to you.

**Best for:**  
- Licensing requirements (e.g., Windows, SQL Server)
- Regulatory or compliance constraints

**Pros:**  
✔ Full hardware isolation

**Cons:**  
✖ Higher cost

---

## 🧑‍💻 6. **Dedicated Instances**
**What it is:**  
Instances run on hardware dedicated to a single customer.

**Best for:**  
- Isolation at the host level

**Pros:**  
✔ Isolated from other AWS accounts

**Cons:**  
✖ Not as flexible as Shared tenancy

---

## ⚡ 7. **Capacity Reservations**
**What it is:**  
Reserve capacity in a specific AZ for later use.

**Best for:**  
- Guaranteed capacity requirements

**Pros:**  
✔ Ensures you can launch when you need it

**Cons:**  
✖ You pay whether you use it or not

---

# 💡 When to Use Which (Exam Logic)

| Situation | Best Option |
|-----------|-------------|
| Predictable long-term workload | *Savings Plans / Reserved Instances* |
| Short-term or unpredictable | *On-Demand* |
| Cost-sensitive, fault-tolerant | *Spot Instances* |
| Licensing & compliance | *Dedicated Hosts* |
| Must reserve capacity | *Capacity Reservations* |

---

# 🧠 Exam Tips

✅ **Savings Plans > Reserved Instances** for flexibility  
✅ **Spot** is cheapest but *interruptible*  
✅ **On-Demand** has no commitment  
✅ **Dedicated Hosts** are for specific compliance/licensing

---

# Examples

```text
✔ Analytics batch jobs → Spot
✔ Production web servers → Savings Plans
✔ R&D / testing → On-Demand
✔ Legacy app with per-CPU licensing → Dedicated Host
