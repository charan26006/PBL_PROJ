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

\[
D =
\begin{bmatrix}
0 & 6 & 0 & 0 & 12 & 0 & 22 & 0 & 7 & 0 \\
6 & 0 & 6 & 15 & 0 & 10 & 0 & 0 & 5 & 0 \\
0 & 6 & 0 & 18 & 0 & 0 & 0 & 4 & 0 & 4 \\
0 & 15 & 18 & 0 & 0 & 0 & 0 & 0 & 0 & 16 \\
12 & 0 & 0 & 0 & 0 & 6 & 0 & 0 & 19 & 0 \\
0 & 10 & 0 & 0 & 6 & 0 & 0 & 0 & 0 & 8 \\
22 & 0 & 0 & 0 & 0 & 0 & 0 & 4 & 0 & 16 \\
0 & 0 & 4 & 0 & 0 & 0 & 4 & 0 & 4 & 8 \\
7 & 5 & 0 & 0 & 19 & 0 & 0 & 4 & 0 & 8 \\
0 & 0 & 0 & 16 & 0 & 8 & 16 & 8 & 8 & 0
\end{bmatrix}
\]

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

1. User inputs:
   - **Start** and **Destination** locations  
   - **Time of day**
2. System maps the inputs to **graph nodes**
3. Dijkstra’s Algorithm finds the **shortest route**
4. Travel time is computed based on **current speed limit**
5. Displays **top 3 optimal routes**

---

## 💻 Project Setup

### 🧾 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/Traffic-Management-System.git
cd Traffic-Management-System
