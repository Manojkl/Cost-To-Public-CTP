# Road Infrastructure of Bangalore

In the 2024-25 fiscal year, the Bruhat Bengaluru Mahanagara Palike (BBMP) allocated over ₹2,130 crore for road-related projects, surpassing allocations for healthcare, education, and welfare. 

Additionally, the Urban Development Department approved a ₹694 crore plan to resurface approximately 390 km of roads, with work commencing in January 2025. 

The Bangalore Development Authority (BDA) is advancing the Peripheral Ring Road project, securing a ₹27,000 crore loan from the Housing and Urban Development Corporation. Of this, ₹21,000 crore is designated for land acquisition, and ₹6,000 crore for road construction. 

These initiatives reflect significant investments by both BBMP and BDA to enhance Bengaluru's road infrastructure. 

## Collect the data

- Data on conditions of roads in Bangalore
- Expenditure spending data on Roads
- Corruption data on Road Infrastructure
- Create the database

In Bengaluru, the maintenance and development of roads are primarily managed by two agencies: the Bruhat Bengaluru Mahanagara Palike (BBMP) and the Bangalore Development Authority (BDA).

**Bruhat Bengaluru Mahanagara Palike (BBMP):**

BBMP is responsible for the city's municipal infrastructure, including road maintenance within its jurisdiction. Key officials overseeing road infrastructure include:

- **Chief Engineer (Major Roads):** This position oversees the maintenance and development of major arterial and sub-arterial roads across various zones. 

- **Executive Engineers:** Each zone has Executive Engineers responsible for specific divisions. For example:

  - **Sri. Nandeesh J.R:** Executive Engineer (Road Widening) 

  - **Sri. Praveen Lingaiah:** Executive Engineer (TEC) 

Additionally, each zone has a Chief Engineer overseeing all engineering works, including road maintenance. For instance:

- **South Zone:**

  - **Chief Engineer:** Shri. Rajesh S.V. 

- **West Zone:**

  - **Chief Engineer (I/C):** Sri Shashikumar 

**Bangalore Development Authority (BDA):**

BDA is tasked with the planning and development of urban infrastructure, including major road projects like the Peripheral Ring Road. Key officials include:

- **Chairman:** Senior IAS officer Rakesh Singh was appointed as the head of BDA. 

- **Commissioner:** Sri N. Jayaram, I.A.S. 

- **Engineer Member:** Dr. H R Shantharajanna oversees engineering projects within BDA. 

In Karnataka, the maintenance and development of Bengaluru's road infrastructure fall under the purview of the Urban Development Department (UDD) and the Directorate of Municipal Administration (DMA). The ministers responsible for these departments are:

- **Urban Development Minister:** Sri Suresha B.S. 

- **Municipal Administration Minister:** Sri Rahim Khan. 

These ministers oversee the planning, development, and maintenance of urban infrastructure, including roads, in Bengaluru. 

These officials are instrumental in the planning, execution, and maintenance of Bengaluru's road infrastructure, ensuring the city's transportation network is developed and maintained effectively. 

# Cost of storing the Road data

If only **video** and **metadata** are collected for the entire **6.7 million kilometers** of India's road network, the total memory required and the cost to store the data can be calculated as follows:

---

### **Key Assumptions**
1. **Video Specifications**:
   - Resolution: HD (1080p) at 30 FPS, compressed using H.264/HEVC.
   - Size: ~120 MB per kilometer.
   - Duration: Average inspection speed of 30 km/h.

2. **Metadata**:
   - Includes GPS coordinates, timestamps, and annotations.
   - Size: ~1 MB per kilometer.

3. **Road Network Length**: 6.7 million kilometers.

4. **Storage Options**:
   - **Cloud storage** costs (e.g., AWS, Google Cloud, Azure).  
   - On-premises storage costs (for local storage).

---

### **Storage Requirements**

#### **Per Kilometer Data**
- **Video**: ~120 MB.  
- **Metadata**: ~1 MB.  
- **Total per km**: **121 MB**.

#### **For 6.7 Million Kilometers**
- Total data = \( 6.7 \times 10^6 \times 121 \, \text{MB} \)  
- Total data = **810,700,000 MB** = **810.7 TB (terabytes)** ≈ **0.81 PB (petabytes)**.

---

### **Estimated Storage Costs**

#### **Cloud Storage**
1. **AWS S3 (Standard Tier)**:
   - Cost: ~$23/TB/month.
   - Monthly cost: \( 810.7 \, \text{TB} \times 23 = \) **$18,646/month**.
   - Annual cost: ~**$223,752/year**.

2. **Google Cloud Storage (Standard)**:
   - Cost: ~$20/TB/month.
   - Monthly cost: \( 810.7 \, \text{TB} \times 20 = \) **$16,214/month**.
   - Annual cost: ~**$194,568/year**.

3. **Azure Blob Storage (Hot Tier)**:
   - Cost: ~$21/TB/month.
   - Monthly cost: \( 810.7 \, \text{TB} \times 21 = \) **$17,024/month**.
   - Annual cost: ~**$204,288/year**.

#### **On-Premises Storage**
- Assuming **$200/TB** for storage hardware (initial cost).
- Storage cost: \( 810.7 \, \text{TB} \times 200 = \) **$162,140**.
- Additional costs: Maintenance, electricity, and cooling (~20-30% annually).

---

### **Summary of Costs**

| Storage Type         | Monthly Cost  | Annual Cost  | Initial Cost  |
|----------------------|---------------|--------------|---------------|
| AWS S3 (Standard)    | $18,646       | $223,752     | N/A           |
| Google Cloud Storage | $16,214       | $194,568     | N/A           |
| Azure Blob Storage   | $17,024       | $204,288     | N/A           |
| On-Premises          | N/A           | ~$32,428*    | $162,140      |

_*Annual maintenance cost for on-premises storage._

---

### **Key Considerations**
1. **Compression**: Use advanced codecs like H.265 to reduce storage requirements by 30-50%.  
2. **Cold Storage**: For archival purposes, cloud providers offer cheaper options like AWS Glacier (~$4/TB/month).  
3. **Scalability**: Cloud storage is more scalable for large projects.  
4. **Network Costs**: Uploading large datasets to the cloud involves additional data transfer costs.

# Optimized cost

To calculate the **optimized cost** for storing the video and metadata from a road inspection system of India's 6.7 million km network, including **compression**, **cold storage options**, and other optimizations, let’s break it down:

---

### **Key Optimizations**
1. **Video Compression**:
   - Use **H.265/HEVC** compression, which is 30-50% more efficient than H.264.
   - Post-compression video size: ~60 MB per kilometer (down from 120 MB).
   - Metadata remains unchanged at ~1 MB per kilometer.
   - Total data per km: **61 MB**.

2. **Cold Storage**:
   - Store data in **cold storage tiers** (AWS Glacier, Azure Cool Blob, etc.), which are much cheaper than standard storage for infrequently accessed data.

3. **Archival Strategy**:
   - Store only the latest dataset in active storage (20% of the data).  
   - Move older datasets to cold storage.  
   - Retain data in cold storage for long-term archival.

---

### **Revised Storage Requirements**
#### **Compressed Data Volume**
- Per kilometer: 61 MB.  
- For 6.7 million km: \( 6.7 \times 10^6 \times 61 \) MB = **408,700,000 MB** = **408.7 TB**.

#### **Active vs Cold Storage Split**
- Active storage (20%): \( 408.7 \times 0.2 = 81.74 \, \text{TB} \).  
- Cold storage (80%): \( 408.7 \times 0.8 = 326.96 \, \text{TB} \).  

---

### **Optimized Cost Estimates**

#### **1. Cloud Storage**
##### **Active Data (20%)**:
- **AWS S3 Standard** (~$23/TB/month):
  - Cost: \( 81.74 \times 23 = \) **$1,880/month** = **$22,560/year**.

##### **Cold Data (80%)**:
- **AWS Glacier Deep Archive** (~$1/TB/month):
  - Cost: \( 326.96 \times 1 = \) **$327/month** = **$3,924/year**.

##### **Total Cloud Cost**:
- Monthly: \( 1,880 + 327 = \) **$2,207/month**.
- Annual: **$26,484/year**.

---

#### **2. On-Premises Storage**
##### **Hardware Cost**:
- Compressed total data: **408.7 TB**.  
- Storage cost: \( 408.7 \times 200 = \) **$81,740 (one-time)**.  

##### **Annual Maintenance**:
- Estimated at 20% of hardware cost: \( 81,740 \times 0.2 = \) **$16,348/year**.

##### **Total On-Premises Cost**:
- **Year 1**: **$98,088** (includes hardware + maintenance).  
- **Subsequent Years**: **$16,348/year**.

---

### **Optimized Cost Summary**

| Storage Type           | Year 1 Cost        | Annual Cost (Post Year 1) |
|------------------------|--------------------|---------------------------|
| **Cloud Storage**      | $26,484           | $26,484                   |
| **On-Premises Storage**| $98,088           | $16,348                   |

---

### **Key Considerations for Cost Optimization**
1. **Cloud vs On-Premises**:  
   - **Cloud** is better for scalability and low upfront investment.  
   - **On-premises** becomes cost-effective over the long term but requires significant initial investment.

2. **Further Compression**: Using more aggressive compression techniques or lower resolutions (e.g., 720p) can further reduce costs.

3. **Data Retention Policy**: Regularly purge or archive outdated data to reduce storage needs.

To calculate the amount of data required to store road inspection data for the **average road length in a panchayat (~27 km)** in India, here’s the breakdown:

---

### **Key Assumptions**
1. **Road Length**: 27 km per panchayat.
2. **Data Types**:  
   - **Video**: HD video at 30 FPS, compressed using H.265 (~60 MB per kilometer).  
   - **Metadata**: GPS coordinates, timestamps, etc. (~1 MB per kilometer).

3. **Data Per Kilometer**:
   - Video: 60 MB.  
   - Metadata: 1 MB.  
   - Total per kilometer: **61 MB**.

4. **Number of Panchayats**: 250,000.

---

### **Data Per Panchayat**
- Road length: 27 km.  
- Data for 27 km = \( 27 \times 61 \, \text{MB} = 1,647 \, \text{MB} \) = **~1.65 GB**.

---

### **Data for All Panchayats**
- Total data = \( 250,000 \times 1.65 \, \text{GB} = 412,500 \, \text{GB} \).  
- Total = **412.5 TB**.

---

### **Storage Optimization**
1. **Compression**: Further compression could reduce the storage requirement to ~50% (e.g., with advanced codecs or lower resolutions).  
   - Compressed size: ~206 TB.

2. **Cold Storage**:
   - Storing rarely accessed data in cold storage (e.g., AWS Glacier) can reduce costs significantly.  

---

### **Final Storage Estimate**
- **Raw Data**: ~412.5 TB.  
- **With Compression**: ~206 TB.  

## Storage option

- Either use centralized system where all data will be stored and accessed, viewed by public/government
- Store data in individual Panchayat that want's to store the data and connect all the panchayat into a single system to acess/view the data by public/government.
- Any individual can also host the data.
- Create a system to auto inspect the data and give report on the same.


