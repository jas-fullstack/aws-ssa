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

---

## 🔥 Quick Decision Rule (Memorize This)