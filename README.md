# 🚦 Traffic Management System (Java)

A Java-based Traffic Management System that applies **Dijkstra’s Algorithm** to determine the **shortest and fastest routes** between major areas in Bangalore.  
The system dynamically adjusts **travel time** based on the **time-of-day speed limit** and visualizes the **road network graph**.

---

## 🧩 Features

- Dijkstra’s **Shortest Path Algorithm**
- **Time-based** traffic speed adjustments
- Displays **Top 3 optimal routes**
- Uses a **distance matrix representation**
- Graph visualization using **JGraphT** and **JGraphX**

---

## 🗺️ City Distance Matrix

Let the locations be represented as follows:

| Index | Location |
|:------:|:----------|
| 0 | Majestic |
| 1 | MG Road |
| 2 | Koramangala |
| 3 | Whitefield |
| 4 | Indiranagar |
| 5 | Jayanagar |
| 6 | Banashankari |
| 7 | Banaswadi |
| 8 | Vidhana Soudha |
| 9 | RT Nagar |

The **distance matrix** (in km) is:

### Distance Matrix (in km)

```python
D = [
    [ 0,  6,  0,  0, 12,  0, 22,  0,  7,  0],
    [ 6,  0,  6, 15,  0, 10,  0,  0,  5,  0],
    [ 0,  6,  0, 18,  0,  0,  0,  4,  0,  4],
    [ 0, 15, 18,  0,  0,  0,  0,  0,  0, 16],
    [12,  0,  0,  0,  0,  6,  0,  0, 19,  0],
    [ 0, 10,  0,  0,  6,  0,  0,  0,  0,  8],
    [22,  0,  0,  0,  0,  0,  0,  4,  0, 16],
    [ 0,  0,  4,  0,  0,  0,  4,  0,  4,  8],
    [ 7,  5,  0,  0, 19,  0,  0,  4,  0,  8],
    [ 0,  0,  0, 16,  0,  8, 16,  8,  8,  0]
]
```

Each element \( D[i][j] \) represents the **distance (km)** between location *i* and *j*.

---

## ⏱️ Speed Limits by Time of Day

| Time of Day | Average Speed (km/h) |
|--------------|----------------------|
| Morning      | 15 |
| Afternoon    | 25 |
| Evening      | 15 |
| Night        | 20 |

---

## ⚙️ How It Works

## ⚙️ How It Works

1. **User Inputs:**  
   - Start and destination locations  
   - Time of day  

2. **System Processing:**  
   - Maps the inputs to corresponding graph nodes  
   - Executes **Dijkstra’s Algorithm** to find the shortest route  
   - Computes travel time based on current speed limits  

3. **Output:**  
   - Displays the **Top 3 Optimal Routes**


---

## 💻 Project Setup

### 🧾 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/Traffic-Management-System.git
cd Traffic-Management-System
```
## 📦 2. Add Dependencies

The project requires the following external libraries:

| Library | Purpose |
|----------|----------|
| **JGraphT (v1.5.1)** | Graph structure and Dijkstra’s algorithm |
| **JGraphX (v4.2.2)** | Graph visualization |

📂 **Setup:**  
Download the `.jar` files and place them inside the `lib/` folder of your project.

**Classpath Example:**

```bash
javac -cp ".;lib/jgrapht-core-1.5.1.jar;lib/jgraphx-4.2.2.jar" TrafficManagementSystem.java
```
## ▶️ 3. Run the Program

To compile and execute the program, use the following commands in your terminal:

```bash
javac -cp ".;lib/jgrapht-core-1.5.1.jar;lib/jgraphx-4.2.2.jar" TrafficManagementSystem.java
java -cp ".;lib/jgrapht-core-1.5.1.jar;lib/jgraphx-4.2.2.jar" TrafficManagementSystem
```

---
## 🧮 Example Output

**Enter the start location:** Majestic  
**Enter the destination location:** Koramangala  
**Enter time of day (morning, afternoon, evening, night):** afternoon  

**Top 3 Shortest Routes from Majestic to Koramangala:**

1. **Distance:** 6 km  |  **Time:** 14.4 mins  
2. **Distance:** 10 km |  **Time:** 24.0 mins  
3. **Distance:** 12 km |  **Time:** 28.8 mins


## 📊 Graph Visualization

Below is a sample graph visualization generated using **JGraphX**.

Each node represents a **location**, and edges denote **road distances (in km)**.  
The highlighted path indicates the **shortest route** computed using **Dijkstra’s Algorithm**.

---

## 🧠 Methodology

| Step | Description |
|------|--------------|
| **1. Data Collection** | Derived a distance matrix from inter-area connectivity. |
| **2. Graph Representation** | Each location is a vertex; road distances are weighted edges. |
| **3. Algorithmic Optimization** | Applied Dijkstra’s Algorithm for shortest path computation. |
| **4. Speed Adjustment** | Adjusted average speed based on the time-of-day factor. |
| **5. Visualization & Output** | Displayed top three shortest routes along with the visualized graph. |

---

## 🧰 Technologies Used

| Component | Description |
|------------|--------------|
| **Java (JDK 17+)** | Core programming language used for development |
| **JGraphT** | Library for graph operations and algorithms |
| **JGraphX** | Library for graph visualization |
| **Java Collections Framework** | For data storage and manipulation |

---

## 🚀 Future Scope

- Integration with **real-time traffic APIs**  
- Implementation of **A\*** and **Bellman-Ford** algorithms  
- Development of a **GUI dashboard** with live map rendering  
- Addition of a **database layer** for road data persistence  

---

## 👨‍💻 Authors

**Gurucharan P**  
- 📧 guru.p.charan@gmail.com  
- 🔗 [GitHub Profile](https://github.com/charan26006)

**Gorla Sai Praneeth Reddy**
- 📧 saipraneeth1806@gmail.com 
- 🔗 [GitHub Profile](https://github.com/saipraneeth88)
