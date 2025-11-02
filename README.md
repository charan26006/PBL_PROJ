# 🚦 Traffic Management System (Java)

A Java-based Traffic Management System that uses **Dijkstra’s Algorithm** to find the **shortest routes** between major areas in Bangalore.  
The system adjusts travel time based on **time-of-day traffic speed limits** and includes a **graph visualization** of the city’s road network.

---

## 🧩 Features

- Implements **Dijkstra’s shortest path algorithm**
- Considers **time-of-day speed limits**
- Displays **top 3 shortest routes** between any two locations
- Uses a **distance matrix** for route mapping
- Visualizes the **road network graph** using `JGraphT` and `JGraphX`

---

## 🗺️ City Distance Matrix

| Locations | Majestic | MG Road | Koramangala | Whitefield | Indiranagar | Jayanagar | Banashankari | Banaswadi | Vidhana Soudha | RT Nagar |
|------------|-----------|----------|--------------|-------------|--------------|-------------|---------------|--------------|------------|
| **Majestic** | 0 | 6 | 0 | 0 | 12 | 0 | 22 | 0 | 7 | 0 |
| **MG Road** | 6 | 0 | 6 | 15 | 0 | 10 | 0 | 0 | 5 | 0 |
| **Koramangala** | 0 | 6 | 0 | 18 | 0 | 0 | 0 | 4 | 0 | 4 |
| **Whitefield** | 0 | 15 | 18 | 0 | 0 | 0 | 0 | 0 | 0 | 16 |
| **Indiranagar** | 12 | 0 | 0 | 0 | 0 | 6 | 0 | 0 | 19 | 0 |
| **Jayanagar** | 0 | 10 | 0 | 0 | 6 | 0 | 0 | 0 | 0 | 8 |
| **Banashankari** | 22 | 0 | 0 | 0 | 0 | 0 | 0 | 4 | 0 | 16 |
| **Banaswadi** | 0 | 0 | 4 | 0 | 0 | 0 | 4 | 0 | 4 | 8 |
| **Vidhana Soudha** | 7 | 5 | 0 | 0 | 19 | 0 | 0 | 4 | 0 | 8 |
| **RT Nagar** | 0 | 0 | 0 | 16 | 0 | 8 | 16 | 8 | 8 | 0 |

---

## ⏱️ Speed Limits by Time of Day

| Time of Day | Average Speed (km/h) |
|--------------|----------------------|
| Morning      | 15                   |
| Afternoon    | 25                   |
| Evening      | 15                   |
| Night        | 20                   |

---

## ⚙️ How It Works

1. User enters:
   - **Start location**
   - **Destination location**
   - **Time of day (morning, afternoon, evening, night)**
2. The system maps locations to graph nodes.
3. Dijkstra’s algorithm computes the shortest path.
4. Speed limit (based on time of day) is used to estimate total travel time.
5. Displays **Top 3 shortest routes** with distance and time.

---

## 💻 Execution Steps

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/Traffic-Management-System.git
cd Traffic-Management-System
