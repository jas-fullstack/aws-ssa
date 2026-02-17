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
